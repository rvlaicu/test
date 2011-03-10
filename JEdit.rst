================================================================================
Using jEdit with Rails
================================================================================

At the moment, I'm playing around with jEdit.   
 
 * After downloading and installing it, I configured it with these settings:
  <a
   href="http://www.tanguay.info/web2008/tutorial.php?idCode=rubyOnRails&sectionIdCode=configureJEditForRuby">Configure
   jEdit for Ruby</a>  
 
It took me a while to find it, but to access your files, there's a File
 Browser System that's invisible or collapsed to the side by default. If it's
 not there, try:  
 
 * Utilities &gt; File System Browser. There should be an option for you to dock it somewhere in the main window.  
 
Rails 2.1.* started naming the view files *.html.erg instead of *.rhtml. This caused the view files to lose its syntax highlighting. To get jEdit to recognize the new extension:  
 
 * Utilities &gt; Global Options &gt; Editing. In the "Change settings for mode", select "rhtml".  
 * Uncheck "user default settings".  
 * Under File name glob, change `*.rhtml` to `*.{rhtml,html.erb}`  
 * Apply   