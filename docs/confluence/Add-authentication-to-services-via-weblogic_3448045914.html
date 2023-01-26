<!DOCTYPE html>
<html>
    <head>
        <title> Add authentication to services via weblogic</title>
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
                             Add authentication to services via weblogic
                        </span>
                    </h1>
                </div>

                <div id="content" class="view">
                    <div class="page-metadata">
                        
        
    
        
    
        
        
            Created by <span class='author'> Harsh Sohni</span>, last modified on Dec 24, 2021
                        </div>
                    <div id="main-content" class="wiki-content group">
                    <h1 id="Addauthenticationtoservicesviaweblogic-ChangesinWARfile">Changes in WAR file</h1><ul><li><p>Modify the WEB-INF → web.xml file. Add the following tags</p></li></ul><div class="code panel pdl" style="border-width: 1px;"><div class="codeContent panelContent pdl">
<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: java; gutter: false; theme: Confluence" data-theme="Confluence">&lt;security-constraint&gt;
	&lt;web-resource-collection&gt;
		&lt;web-resource-name&gt;secure&lt;/web-resource-name&gt;
		&lt;url-pattern&gt;/&lt;/url-pattern&gt;
	&lt;/web-resource-collection&gt;
	&lt;auth-constraint&gt;
		&lt;role-name&gt;authenticated-users&lt;/role-name&gt;
	&lt;/auth-constraint&gt;
&lt;/security-constraint&gt;
&lt;security-role&gt;
	&lt;description&gt;Authenticated Users&lt;/description&gt;
	&lt;role-name&gt;authenticated-users&lt;/role-name&gt;
&lt;/security-role&gt;</pre>
</div></div><ul><li>Here the two tags &lt;security-constraint&gt; and &lt;security-role&gt; are used to add authentication layer. The tag &lt;role-name&gt; signifies the type of users that can access the service. Authenticated users translates to only users that can be authenticated are allowed, there are also other roles for different purposes.</li><li>Next we need to add a file named weblogic.xml in the same WEB-INF folder with the following xml code.</li></ul><div class="code panel pdl" style="border-width: 1px;"><div class="codeContent panelContent pdl">
<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: java; gutter: false; theme: Confluence" data-theme="Confluence">&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;wls:weblogic-web-app xsi:schemaLocation=&quot;http://java.sun.com/xml/ns/j2ee http://java.sun.com/xml/ns/j2ee/web-app_2_4.xsd http://www.bea.com/ns/weblogic/90 http://www.bea.com/ns/weblogic/90/weblogic-web-app.xsd&quot; xmlns:wls=&quot;http://www.bea.com/ns/weblogic/90&quot; xmlns=&quot;http://xmlns.oracle.com/weblogic/weblogic-web-app&quot; xmlns:xsi=&quot;http://www.w3.org/2001/XMLSchema-instance&quot;&gt;
	&lt;security-role-assignment&gt;
		&lt;role-name&gt;authenticated-users&lt;/role-name&gt;
		&lt;principal-name&gt;CustomerService&lt;/principal-name&gt;
	&lt;/security-role-assignment&gt;
&lt;/wls:weblogic-web-app&gt;</pre>
</div></div><ul><li>Here role-name again signifies the type of users that can access and principal-name signifies the name of the group of users that can access the service.</li><li>After completion update the deployment via weblogic console.</li></ul><h1 id="Addauthenticationtoservicesviaweblogic-Addinguserviaweblogicconsole"> Adding user via weblogic console</h1><p><br/></p><ul><li>In weblogic console traverse to<span style="color: rgb(0,0,0);"> </span>Home &gt;Summary of Security Realms &gt;myrealm &gt;Users and Groups here you can create a new user</li></ul><p>         <span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" draggable="false" height="400" src="attachments/3448045914/3448046105.png" data-image-src="attachments/3448045914/3448046105.png" data-unresolved-comment-count="0" data-linked-resource-id="3448046105" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2021-12-24_10-56-50.png" data-base-url="https://confluence.oraclecorp.com/confluence" data-linked-resource-content-type="image/png" data-linked-resource-container-id="3448045914" data-linked-resource-container-version="3"></span></p><ul><li>Similarly you can also create a user group with the same name as given previously in the principal-name tag of weblogic.xml.</li></ul><p>          <span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" draggable="false" height="150" src="attachments/3448045914/3448046126.png" data-image-src="attachments/3448045914/3448046126.png" data-unresolved-comment-count="0" data-linked-resource-id="3448046126" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2021-12-24_11-1-56.png" data-base-url="https://confluence.oraclecorp.com/confluence" data-linked-resource-content-type="image/png" data-linked-resource-container-id="3448045914" data-linked-resource-container-version="3"></span></p><ul><li>Lastly assign the user a group by clicking on the user and adding it to a group.</li></ul><p>          <span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" draggable="false" height="250" src="attachments/3448045914/3448046136.png" data-image-src="attachments/3448045914/3448046136.png" data-unresolved-comment-count="0" data-linked-resource-id="3448046136" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2021-12-24_11-3-58.png" data-base-url="https://confluence.oraclecorp.com/confluence" data-linked-resource-content-type="image/png" data-linked-resource-container-id="3448045914" data-linked-resource-container-version="3"></span></p><ul><li>We can now go and check the wadl for the service and see if we are asked for authenticating before entering.</li></ul><p>         <span class="confluence-embedded-file-wrapper confluence-embedded-manual-size"><img class="confluence-embedded-image" draggable="false" height="250" src="attachments/3448045914/3448046148.png" data-image-src="attachments/3448045914/3448046148.png" data-unresolved-comment-count="0" data-linked-resource-id="3448046148" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2021-12-24_11-6-8.png" data-base-url="https://confluence.oraclecorp.com/confluence" data-linked-resource-content-type="image/png" data-linked-resource-container-id="3448045914" data-linked-resource-container-version="3"></span></p>
                    </div>

                                                            <div class="pageSection group">
                        <div class="pageSectionHeader">
                            <h2 id="attachments" class="pageSectionTitle">Attachments:</h2>
                        </div>

                        <div class="greybox" align="left">
                                                            <img src="images/icons/bullet_blue.gif" height="8" width="8" alt=""/>
                                <a href="attachments/3448045914/3448046105.png">image2021-12-24_10-56-50.png</a> (image/png)
                                <br/>
                                                            <img src="images/icons/bullet_blue.gif" height="8" width="8" alt=""/>
                                <a href="attachments/3448045914/3448046126.png">image2021-12-24_11-1-56.png</a> (image/png)
                                <br/>
                                                            <img src="images/icons/bullet_blue.gif" height="8" width="8" alt=""/>
                                <a href="attachments/3448045914/3448046136.png">image2021-12-24_11-3-58.png</a> (image/png)
                                <br/>
                                                            <img src="images/icons/bullet_blue.gif" height="8" width="8" alt=""/>
                                <a href="attachments/3448045914/3448046148.png">image2021-12-24_11-6-8.png</a> (image/png)
                                <br/>
                                                    </div>
                    </div>
                    
                                                      
                </div>             </div> 
            <div id="footer" role="contentinfo">
                <section class="footer-body">
                    <p>Document generated by Confluence on Jan 26, 2023 11:18</p>
                    <div id="footer-logo"><a href="http://www.atlassian.com/">Atlassian</a></div>
                </section>
            </div>
        </div>     </body>
</html>
