
# Proofreader Guide

* **Original text:** When getting ready to proofread, open the appropriate page on the Globasa website in order to reference it when the occasion arises.  
* **Color-coded text:** Ignore the text in red and blue. Hector will take care of the text in blue. Only concern yourself with black and purple text. Do **not** attempt to change the color of any of the text. Do **not** change any of the spacing either.      
* **Target language text:** You will mostly be proofreading the text in the target language. Make corrections not only to obvious target language errors, but also make sure the text makes sense in the target language, as well as make any edits to improve wording or other minor errors.   
* **Globasa text:** Some, but not all Globasa text has been reviewed by Hector beforehand, so this should mostly not be an issue. Still, be sure to also review Globasa text to make sure Google Translate didn't assume it to be English and attempt to translate it into the target language or otherwise alter the spelling. Text in Globasa is usually easy to spot since it's most often encapsulated in double asterisks, at the start and at the end of the word/phrase/sentence.  
*  **Word for "Globasa" in the target language**
 * **Spanish:** - Globasa
 * **Esperanto:** - Globaso 


# Contributor Guide

Quick links: [Main site admin](https://www.globasa.net/admin), [Doxo admin](https://doxo.globasa.net/admin), [Xwexi admin](https://xwexi.globasa.net/admin).

<a href="https://info.flagcounter.com/AWBh"><img src="https://s11.flagcounter.com/map/AWBh/size_s/txt_000000/border_CCCCCC/pageviews_0/viewers_3/flags_0/" alt="Flag Counter" border="0"></a>

Soon, these will be changed to using GitHub. (At which point the above links won't work.)

There are several ways contributors can contribute:

* Editing the Globasa.net websites (main, Doxo and Xwexi)
* Translating websites (main, Doxo and Xwexi)
* Adding and moderating content on the Wiki & Reddit
* Other special projects, like in the past: making graphics, audio, etc.

All contributors should learn what Markdown formatting is, as used in Grav and Reddit, and possibly Wiki formatting, for adding to the Wiki.

So far this guide is just for people doing website stuff. But that should be in it's own Grav Tips for Website Editors (translators and content management).




## Tips for Website Editors

Common information for people editing the Globasa websites:

Each page can have a separate version for every language. You can switch between languages when editing by clicking the purple flag language button. If there is not a down arrow to change languages, you will need to create a new translation. Click the down arrow on the purple save button and choose the language to copy the page to.

### Create a new page

To create a new page on Xwexi, Doxo or the main site:

1. Login as Admin
2. Selected Pages on the left-hand menu.
3. Press the “+ Add” button
4. Select the parent page, set visible to yes.
     - ℹ️ If this step is missed, you will need to go to expert mode and set add `visible: true` to the page properties above the content.
5. Create the page, add some content, and save it.
6. Note that next to the page name, you will see the page filename (the URL). Note the last part, which should be the same as the name, but with hyphens rather than spaces.
7. In many cases, you will need to add a link to the new page in the parent page. Eg., when creating ‘Word Classes’, go to Grammar and make a link by types `[Word Classes](word-classes)`
     - In the square brackets, type the name of the page or some other description. This is what the readers will see while on the page.
     - In the round brackets, you must enter the filename of the newly created page.
8. Next, you must force the website to update the menus, so the new page will appear. To do this, click the ‘clear cache’ button on the left-hand menu under your username. It should have two arrows circling around each other. 🔁

### Page URL

The page URL is the 'Folder Name' in the 'Advanced' tab.

! There is a 'Slug Override' in the override section, but ideally that is not used and unchecked. But check it if something isn't working.

### Page Title and Menu name
The page 'Title' in the 'Content' tab is what is used in the Menu. Each Title for every language is the one used in that languages' menu.

! There is a 'Menu' in the override section of the 'Advanced' tab, but ideally that is not used and unchecked. But check it if something isn't working.

### Hide a page

If you are asking how to hide a page from the site menu, it's like this: go to 'Advanced' and scroll down near the bottom of the Overrides section and select the checkbox for 'Visible' and set it to 'No'. This will override the visibility and make it, so it doesn't get listed. Alternatively, you could say the page is not published under options.

### External website redirects

Some menu links don't bring up pages, but redirect people to another website. In particular, the link to Learn, Read, and Wiki. There is probably a better way to do this, but what I've done is created a page that redirects. To change this item in the menu, the page (Learn, Read, Wiki) and follow the page title and menu name section above. To change the redirect go to the language you want to change the redirect for, go to the 'Advanced' tab, and in the 'Overides' section change 'Page redirect' text box to whatever you want it to be.

### Page metadata

Web pages have data about the page hidden in them, which is used for website, search engines and apps to display information about the page in a thumbnail or search result. Any page that does not have metadata set for it will use the site-wide default.

#### Page description metadata

The **description** is the blurb that describes the page and is shown on thumbnail links when sharing a page and on search results. 

Every page should have it's own description, for each language the page is translated in to. _To change the page page description_:

![page-description](page-description.png "Screenshot of the publishing section.")

* open the page for editing,

* click the 'options' tab at the top,

* make sure 'metadata' is checked,

* add a metadata item for 'description' if there isn't one:
	* click the plus button,
	* type 'description' in the keyword input box,
	* type in what you want shown in the value input box.

* or, edit the description value input box.


_To change the site wide default page description_, someone with Admin access needs to sign in to the admin panel and then:

![site-description](site-description.png "Screenshot of the metadata section.")

* select 'Configuration' on navigation menu,

* then the 'Site' tap at the top,

* then scroll down to Metadata,

* find the 'description' metadata keyword/name (currently the only one), and edit the 'value' input box, which is next to the input box that says 'description'. (Currently, that's the only one.)
