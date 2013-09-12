jQuery-Transator-Plug-in
=========================

<b>NOTICE</b>:

This plug-in utilizes the free Microsoft Bing Translator API.

Athough Microsoft announced that "As of August 1, 2012 the Bing Translation API will be moved to the Azure Cloud as a paid service," it appears they are still supporting the API that this plug-in is dependant on. Microsoft, however may still cancel this free service without further notice. 

<b>OVERVIEW</b>:

With the jQuery-translator-plug-in, web pages are easily translated into over 30 languages without modifying any HTML. You need only supply script references and initialize the plug-in.

Although Microsoft's Bing Translator API is currently free, they require you register for an Application ID which is easily and instantly obtained (<a href="http://www.microsoft.com/web/post/using-the-free-bing-translation-apis", target="_blank">Getting a Bing AppID</a>).

After the plug-in is initialized, a drop-down list of supported languages (or an optionally defined subset) is added to the upper-right corner of the document (like the one on this page), or at the location of the optionally specified DOM element.

The translation is performed for all specified jQuery selectors. Any element that contains inner text (p,span,a,...) or the input element (type 'text' or 'button') can be included in the selection. Note that translations are context based, so “phrases” are more accurately translated than short descriptions (headings, menu items, buttons, etc.). For example, “General Information” or "Order Date” are too ambiguous to translate accurately in all supported languages.

<b>INSTALLATION</b>
<p>Download the plug-in.</p>
<p><b>Provide Script References like the following:</b></p>
    <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.6/jquery.min.js"></script>
    <script type="text/javascript" src="js/jquery.translator-ms-1.0.0.min.js"></script>


<p><b>Initialize the <i>translator</i> plug-in</b></p>
<p>Call the <i>translator</i> initialize function specifying the jQuery selectors (DOM node names, (.) classes, (#) element ids, etc.) containing the text you want translated. Your Bing AppId must be specified. You can optionally specify a DOM Element to contain the Supported Language List, which is displayed in the language detected by the plug-in or by using the “listLanguage” option. You can also choose not to display the Language List, as well as applying the translation to a specified language using the “tolang” option.</p>

<p><b>OPTIONS</b></p>
<b>appID</b>
<p style="display:inline;">The Microsoft Bing API Application ID you obtained for the website you wish to deploy this plug-in on. <b>(Required)</b></p>

<b>callback</b>
<p style="display:inline;">Function to call after translator completes.</p>

<b>languageListNode</b><p style="display:inline;">DOM Element object that will contain the Supported Languages Drop-Down List (id='_supportedLanguagesList' <b>reserved - do not include this id in your HTML</b>).</p>

<b>languagesList</b><p style="display:inline;">An array of language codes to display in the Drop-Down List.</p>
<b>nolist</b><p style="display:inline;">The Languages Drop Down List is not created or displayed.</p>
<b>listLanguage</b><p style="display:inline;">The 2-4 character code associated with the written language of your web pages, which is used to override the auto-detected language. This parameter only applies to the Languages Drop Down List and not to selected content. </p>
<b>tolang</b><p style="display:inline;">The language code (ex. 'fr') to translate the current page to. The Languages Drop Down List is not affected by this option.</p>
<p>For a list of currently supported language codes: <a href="http://msdn.microsoft.com/en-us/library/hh456380.aspx" target="_blank">Bing Translator Language Codes</a></p>

<b>EXAMPLES</b>
      <p> The following initialization examples illustrate the use of these options.</p>
      <ul>
        <li>$("p,h1,h2,.xlatext,#topic").translator({ appID: BingAppID, languageListNode: $("#languages").get(0) });</li>
        <li>$("p,span").translator({ appID: BingAppID, languagesList: ['en','fr','de','es'] });</li>
        <li>$("p").translator(appID: BingAppID, callback: function() { alert('Do Something') } );</li>
        <li>$("p").translator(appID: BingAppID, tolang: 'fr');</li>
        <li>$("p").translator(appID: BingAppID);</li>
      </ul>
      <p>This page implements the translator by specifying the following statements:</p>
      <div>...</div>
      &lt;head&gt;
      <div>...</div>
        &lt;script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.6/jquery.min.js" ></script><br \>
        /* Assumes you have copied the translator plug-in to a sub-folder named "js" */
        &lt;script type="text/javascript" src="js/jquery.translator-ms-1.0.0.min.js"&gt;&lt;/script&gt;<br \>
        &lt;script type="text/javascript" &gt;<br \>
        $(function ($) { <br \>
                $("p,h1,h2,span").translator({ appId: myBingApiAppId });<br \>
        });<br \>
        &lt;/script&gt;<br \>
      </div>
      <div>...</div>
      &lt;/head&gt;
      <div>...</div>
      <br></br>
      <span>Translate this page using the</span> <a href="javascript:$('#_supportedLanguagesList')[0].focus();">Supported Languages</a> <span>drop-down list, if you haven't done so already.</span><br></br>
      <p>View a customized <i>Supported Lanugages</i> drop-down list <a href="http://msaccess2web.com" target="_blank">example</a>. You can also send emails with your questions, comments and suggestions at this site.</p>
