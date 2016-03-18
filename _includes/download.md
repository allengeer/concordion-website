{% assign spec_type=page.spec_type %}
{% if spec_type == 'html' %}
{% assign html=true %}
{% assign md=false  %}
{% assign spec_type_desc = 'HTML' %}
{% assign ext='html' %}
{% elsif spec_type == 'markdown' %}
{% assign html=false %}
{% assign md=true    %}
{% assign spec_type_desc = 'Markdown' %}
{% assign ext='md'    %}
{% endif %}

{% assign fixture_language=page.fixture_language %}
{% if fixture_language == 'java' %}
{% assign java=true %}
{% assign csharp=false  %}
{% assign fixture_language_desc = 'Java' %}
{% assign supports_2.0 = true %}
{% elsif fixture_language == 'csharp' %}
{% assign java=false %}
{% assign csharp=true %}
{% assign fixture_language_desc = 'C#' %}
{% assign supports_2.0 = false %}
{% endif %}

_This page shows the downloads for __{{ fixture_language_desc }}__._  Click the toggle buttons above to choose other options.

{% if csharp %}
<hr/>
<p><b>TODO:</b> This page has not been translated to C# yet.</p>
<hr/>
{% endif %}

<div class="github-fork-ribbon-wrapper right-bottom">
    <div class="github-fork-ribbon">
        <a href="https://github.com/concordion/concordion">Fork me on GitHub</a>
    </div>
</div>

<div class="row">
    <h1>Latest Release</h1>
    <ul class="collection">
        <li class="collection-item avatar">
        <i class="material-icons circle green">file_download</i>
        <span class="title">Download</span>
        <p>Full distribution including source code and all dependencies:<br>
        <b><a href="http://dl.bintray.com/concordion/downloads/concordion-1.5.1.zip" id="download-link">concordion-1.5.1.zip</a></b> (1.1MB)
        </p>
        </li>
        <li class="collection-item avatar">
        <img src="{{ site.baseurl }}/img/download-gradle.jpg" alt="maven image" class="circle">
        <span class="title">Gradle</span>
        <pre>
        testCompile 'org.concordion:concordion:1.5.1'
        </pre>
        </li>
        <li class="collection-item avatar">
        <img src="{{ site.baseurl }}/img/download-maven.png" alt="maven image" class="circle">
        <span class="title">Maven</span>
        <pre>
        &lt;dependency&gt;
        &lt;groupId&gt;<b>org.concordion</b>&lt;/groupId&gt;
        &lt;artifactId&gt;<b>concordion</b>&lt;/artifactId&gt;
        &lt;version&gt;<b>1.5.1</b>&lt;/version&gt;
        &lt;scope&gt;test&lt;/scope&gt;
        &lt;/dependency&gt;
        </pre>
        </li>
    </ul>
</div>

<div class="row">
    <h1>Release notes</h1>
    <div>
        <p>See our <a href="https://github.com/concordion/concordion/releases">Github release notes</a>.</p>
    </div>
</div>
<div class="row">
    <h1>Extension downloads</h1>
    <div>
        <p>See the Concordion <a href="./extensions">extensions</a> page for download and installation details for extensions.</p>
    </div>
</div>
