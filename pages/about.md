---
layout: page
title: about me
permalink: /about/
weight: 1
---

<script src="https://unpkg.com/@codersrank/activity@0.9.14/codersrank-activity.min.js"></script>
<script src="https://unpkg.com/@codersrank/skills-chart@0.9.21/codersrank-skills-chart.min.js"></script>
<script src="https://unpkg.com/@codersrank/work-experience@0.9.8/codersrank-work-experience.min.js"></script>
<style>
    codersrank-work-experience {
        --date-font-size: 0;
    }
</style>

# **About Me**

Hi! I'm **{{ site.author.name }}** :wave:,<br>

I love designing and building both front end (websites) and back end (APIs) software. I have over 25 years of experience in software development, working for organisations ranging in size from multinational enterprises to a small start-up. I'm a senior developer with a wide range of experience and technical expertise working primarily with C#/.net based software and websites. I have worked on projects ranging in size and complexity, in a variety of different industries.

I have set up a profile on <a href="https://profile.codersrank.io/user/marklnz">CodersRank.io</a> to detail my skills, experience and ongoing coding contributions. My CodersRank profile can be viewed at <a href="https://profile.codersrank.io/user/marklnz">https://profile.codersrank.io/user/marklnz</a>. I use the data from my CodersRank profile below to highlight my skills and experience. Also, my resume is available for download <a href="/resume.pdf">here</a>.

<div class="row">
    <div class="col-lg-4 text-center wow animated fadeIn" data-wow-delay=".15s">
        <div class="project card">
            <div class="card-body text-themed">
                <h5 class="card-title"> 
                    <i class="fab fa-html5"></i>
                    Developing Websites
                </h5>
                <p>With over 20 years of experience using tools like HTML5 and CSS3, Javascript libraries like jQuery and Angular.js, and Microsoft's ASP.Net MVC and WebAPI frameworks, I enjoy building stylish, yet functional, web sites and distributed applications for customers.</p>
            </div>
        </div>
    </div>
    <div class="col-lg-4 text-center wow animated fadeIn" data-wow-delay=".3s">
        <div class="project card">
            <div class="card-body text-themed">
                <h5 class="card-title"> 
                    <i class="fas fa-sitemap"></i>
                    Architecture
                </h5>
                <p>I have software architecture experience at a variety of levels. My experience includes Enterprise Architecture work, as well as work developing software architecture elements, and reviewing architectures designed by others.</p>
            </div>
        </div>
    </div>
    <div class="col-lg-4 text-center wow animated fadeIn" data-wow-delay=".45s">
        <div class="project card">
            <div class="card-body text-themed">
                <h5 class="card-title"> 
                    <i class="fas fa-users-cog"></i>
                    ALM and DevOps
                </h5>
                <p>Years of experience in enterprises has given me a strong understanding of the need for ALM and DevOps. Most recently I've made use of Microsoft's Azure DevOps to build a solid DevOps foundation for my current development team.</p>
            </div>
        </div>
    </div>
</div>

<!-- ## My Coding Activity

Here's what my project contributions over the past year look like. This includes commits to my github projects as well as my activity in the commercial projects I'm working on. This chart forms part of my <a href="https://profile.codersrank.io/user/marklnz">CodersRank.io</a> profile.

<codersrank-activity username="marklnz" labels legend tooltip step="5" branding="false"></codersrank-activity> -->

## My Skills

As the IT industry is constantly changing, I'm always adding new skills to my repertoire. I'm always ready for fresh challenges with new techniques and technologies. The skills I have used most over the past 12 months are shown on the chart below (courtesy of <a href="https://profile.codersrank.io/user/marklnz">CodersRank</a>).

I have much more detail and a more complete list of my skills in my resume, which you can view, download, or print <a href="/resume.pdf">here</a>.

<codersrank-skills-chart username="marklnz" labels="true" legend="true" tooltip="true" skills="C#,Blazor,CSS,HTML,JavaScript,SQL,TSQL,TypeScript" branding="false"></codersrank-skills-chart>

{%- comment -%} Original style skills presentation

<div class="row">
{% include about/skills.html title="Programming Skills" source=site.data.programming-skills %}
{% include about/skills.html title="Other Skills" source=site.data.other-skills %}
</div>
{%- endcomment -%}

<br />

## Professional Experience

I have over 25 years of experience in software development, and have worked for a variety of organisations, large and small. My relevant experience is summarised below (again, courtesy of <a href="https://profile.codersrank.io/user/marklnz">CodersRank</a>). My resume contains full details of my experience. You can download or print a copy <a href="/resume.pdf">here</a>.
<br />
<codersrank-work-experience username="marklnz" branding="false" max-items="3"></codersrank-work-experience>

{%- comment -%} Original style skills presentation

<div class="row">
{% include about/timeline.html %}
</div>
{%- endcomment -%}
