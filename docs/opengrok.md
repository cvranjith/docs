<!DOCTYPE html>
<html>
    <head>
        <title> Using OpenGrok with projects</title>
        <link rel="stylesheet" href="styles/site.css" type="text/css" />
        <META http-equiv="Content-Type" content="text/html; charset=UTF-8">
    </head>

    <body class="theme-default aui-theme-default">
        <div id="page">
            <div id="main" class="aui-page-panel">
                <div id="main-header">
                    <div id="breadcrumb-section">
                        <ol id="breadcrumbs">
                            <li class="first">
                                <span><a href="index.html"></a></span>
                            </li>
                                                    <li>
                                <span><a href="2057266878.html">How To&#39;s</a></span>
                            </li>
                                                </ol>
                    </div>
                    <h1 id="title-heading" class="pagetitle">
                                                <span id="title-text">
                             Using OpenGrok with projects
                        </span>
                    </h1>
                </div>

                <div id="content" class="view">
                    <div class="page-metadata">
                        
        
    
        
    
        
        
            Created by <span class='author'> Sougata Laga</span>, last modified on Mar 25, 2022
                        </div>
                    <div id="main-content" class="wiki-content group">
                    <h3 id="UsingOpenGrokwithprojects-WhatisOpengrok?">What is Opengrok?</h3><p><span style="color: rgb(77,81,86);">OpenGrok is a <strong>source code search and cross reference engine</strong> developed by Oracle Corporation. It helps programmers to search, cross-reference and navigate source code trees to aid code comprehension; and is written in java. </span></p><h3 id="UsingOpenGrokwithprojects-Requisites:">Requisites :</h3><p><strong>Java</strong> 1.8 or higher</p><p>apache <strong>Tomcat</strong></p><p><strong>Opengrok binaries</strong> (from github):  <a class="external-link" href="https://github.com/OpenGrok/OpenGrok/releases" rel="nofollow">https://github.com/OpenGrok/OpenGrok/releases</a></p><p>Universal <strong>Ctags</strong>: <a class="external-link" href="https://github.com/universal-ctags" rel="nofollow">https://github.com/universal-ctags</a></p><p>a <strong>browser,</strong> preferebly chrome.</p><h3 id="UsingOpenGrokwithprojects-Howtoinstall?">How to install?</h3><p>On <strong>linux/ubuntu</strong> : <a class="external-link" href="https://medium.com/@akhilspecials/opengrok-setup-in-linux-ubuntu-a-wicked-fast-source-code-search-engine-345b82277552" rel="nofollow">OpenGrok Setup in Linux Ubuntu. A wicked fast Source Code Search Engine . | by akhilspecials | Medium</a></p><p>On <strong>windows</strong>: <a class="external-link" href="https://medium.com/@kannaapandita/how-to-install-tomcat-and-opengrok-on-windows-e39f7f910348" rel="nofollow">How To Install Tomcat and Opengrok on Windows | by Shuddha Kannadiga | Medium</a></p><p><br/></p><h3 id="UsingOpenGrokwithprojects-GoingwithDocker+containerisedapproach:">Going with Docker+containerised approach: </h3><p><br/></p><p>Using docker, containers make the <strong>process very simple</strong> and easy to handle too. It has to be done in <strong>remote machine,</strong> and not on local pc.</p><p><strong> Steps:</strong> </p><ul><li>login to the required machine in PUTTY. In our case, it was <a class="external-link" href="http://fsgbu-mum-922.snbomprshared1.gbucdsint02bom.oraclevcn.com/" rel="nofollow">fsgbu-mum-922.snbomprshared1.gbucdsint02bom.oraclevcn.com/</a></li><li>login to WINscp also and create folders : /scratch/opengrok/src</li></ul><p>                                                                            /scratch/opengrok/etc</p><p>                                                                            /scratch/opengrok/data</p><ul><li>Give the following docker commands in Putty:</li></ul><p><br/></p><div class="code panel pdl" style="border-width: 1px;"><div class="codeContent panelContent pdl">
<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: java; gutter: false; theme: Confluence" data-theme="Confluence">docker run -d \
    --name opengrok \
    -p 8080:8080 \
    -e SYNC_PERIOD_MINUTES=&quot;60&quot; \
    -v /scratch/opengrok/src:/opengrok/src/ \
    -v /scratch/opengrok/etc/:/opengrok/etc/ \
    -v /scratch/opengrok/data/:/opengrok/data/ \
    opengrok/docker:latest

sudo chmod -R 0777 opengrok/</pre>
</div></div><p><br/></p><ul><li>The server becomes up and running. ( <a class="external-link" href="http://100.76.138.176:8080/" rel="nofollow">http://100.76.138.176:8080/</a>  in our case)</li></ul><p>An interface similar to the one shown below opens up:</p><p><br/></p><p><span class="confluence-embedded-file-wrapper"><img class="confluence-embedded-image" draggable="false" src="attachments/3575244931/3605086240.jpeg" data-image-src="attachments/3575244931/3605086240.jpeg" data-unresolved-comment-count="0" data-linked-resource-id="3605086240" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="pic1.jpeg" data-base-url="https://confluence.oraclecorp.com/confluence" data-linked-resource-content-type="image/jpeg" data-linked-resource-container-id="3575244931" data-linked-resource-container-version="7"></span></p><p>(above img source : google images)</p><p>Other useful<strong> link</strong> : <a class="external-link" href="https://github.com/oracle/opengrok/wiki/How-to-setup-OpenGrok" rel="nofollow">How to setup OpenGrok · oracle/opengrok Wiki · GitHub</a></p><h3 id="UsingOpenGrokwithprojects-Bashscripttoautomatetheupdatingofprojectsindesiredpath:">Bash script to automate the updating of projects in desired path :</h3><p><u><strong>USE CASE : </strong></u>To automatically update the existing projects in the grok, when there is a newer version added, by running a simple bash script. </p><p>The following bash script was written and has to be run after giving the command : <u>export newversion=&quot; ... desired newversion ... &quot;</u> and then run the .sh script</p><p><br/></p><div class="code panel pdl" style="border-width: 1px;"><div class="codeContent panelContent pdl">
<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: java; gutter: false; theme: Confluence" data-theme="Confluence">#!/bin/bash
sudo su jdevopsi
mkdir /scratch/opengrok/src/${newversion}
sudo chown -R jdevopsi /scratch/opengrok/src/${newversion}/
sudo chmod -R 0777 /scratch/opengrok/src/${newversion}/

cd /scratch/opengrok/src
#export newversion = &quot;14.5.0.2.0&quot;
#mkdir $newversion
cd $newversion
ln -s /scratch/odt-upgrade/ELCM/Console/FCELCM_${newversion} /scratch/opengrok/src/${newversion}
ln -s /scratch/odt-upgrade/FCUBS/Console/FCUBS_${newversion} /scratch/opengrok/src/${newversion}
ln -s /scratch/odt-upgrade/OBCL/Console/OBCL_${newversion} /scratch/opengrok/src/${newversion}
ln -s /scratch/odt-upgrade/OBPM/Console/Oracle_Banking_Payments_${newversion} /scratch/opengrok/src/${newversion}
ln -s /scratch/odt-upgrade/OBTF/Console/OBTF_${newversion} /scratch/opengrok/src/${newversion}
ln -s /scratch/odt-upgrade/OBTR/Console/OBTR_${newversion} /scratch/opengrok/src/${newversion}
echo &quot;$newversion folder updated!&quot;
exit 0

</pre>
</div></div><p><br/></p><p>After the script has been run we can see the desired projects are automatically shown/listed in our desired directory. (in this case /opengrok/src)</p><p><br/></p><p>Hope this helps!</p>
                    </div>

                                                            <div class="pageSection group">
                        <div class="pageSectionHeader">
                            <h2 id="attachments" class="pageSectionTitle">Attachments:</h2>
                        </div>

                        <div class="greybox" align="left">
                                                            <img src="images/icons/bullet_blue.gif" height="8" width="8" alt=""/>
                                <a href="attachments/3575244931/3605086240.jpeg">pic1.jpeg</a> (image/jpeg)
                                <br/>
                                                    </div>
                    </div>
                    
                                                      
                </div>             </div> 
            <div id="footer" role="contentinfo">
                <section class="footer-body">
                    <p>Document generated by Confluence on Jan 26, 2023 11:19</p>
                    <div id="footer-logo"><a href="http://www.atlassian.com/">Atlassian</a></div>
                </section>
            </div>
        </div>     </body>
</html>
