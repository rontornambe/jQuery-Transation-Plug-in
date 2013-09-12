jQuery-Transator-Plug-in
=========================

NOTICE:

This plug-in utilizes the free Microsoft Bing Translator API.

Athough Microsoft announced that "As of August 1, 2012 the Bing Translation API will be moved to the Azure Cloud as a paid service," it appears they are still supporting the API that this plug-in is dependant on. Microsoft, however may still cancel this free service without further notice. 

OVERVIEW:

With the jQuery-translator-plug-in, web pages are easily translated into over 30 languages without modifying any HTML. You need only supply script references and initialize the plug-in.

Although Microsoft's Bing Translator API is currently free, they require you register for an Application ID which is easily and instantly obtained (<a href="http://www.microsoft.com/web/post/using-the-free-bing-translation-apis", target="_blank">Getting a Bing AppID</a>).

After the plug-in is initialized, a drop-down list of supported languages (or an optionally defined subset) is added to the upper-right corner of the document (like the one on this page), or at the location of the optionally specified DOM element.

The translation is performed for all specified jQuery selectors. Any element that contains inner text (p,span,a,...) or the input element (type 'text' or 'button') can be included in the selection. Note that translations are context based, so “phrases” are more accurately translated than short descriptions (headings, menu items, buttons, etc.). For example, “General Information” or "Order Date” are too ambiguous to translate accurately in all supported languages.

<h2>Installation</h2>
<p>Download the plug-in.</p>
<p><b>Provide Script References like the following:</b></p>
