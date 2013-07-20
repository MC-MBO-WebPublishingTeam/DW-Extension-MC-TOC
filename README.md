SlideoutTOC.js: create a table of contents for a document.

This module registers an anonymous function that runs automatically when the document finishes loading. When it runs, the function first looks for a document element with an id of "TOC". If there is no such element it creates one at the start of the document.

Next, the function finds all &lt;h1&gt; through &lt;h6&gt; tags, treats them as section titles, and creates a table of contents within the TOC element. The function adds section numbers to each section heading and wraps the headings in named anchors so that the TOC can link to them. The generated anchors have names that begin with "TOC", so you should avoid this prefix in your own HTML.

The entries in the generated TOC can be styled with CSS. All entries have a class "TOCEntry". Entries also have a class that corresponds to the level of the section heading. &lt;h1&gt; tags generate entries of class "TOCLevel1",  &lt;h2&gt; tags generate entries of class "TOCLevel2", and so on. Section numbers inserted into headings have class "TOCSectNum".

That final line generates a colon and space after section numbers. To hide the section numbers, use this:
 .TOCSectNum { display: none }

This module requires the onLoad() utility function.
