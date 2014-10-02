//-----------------------------------------------------------------------------
// [WoD] BBCode generator
//
// Script aimed at players of World Of Dungeons. Generates BBCode for in game forum from the content of the current page
//
// A new button will appear at the left side of each page (below menu).
// Pressing this button will generate BBCode representation of current page and append it at the bottom of the page.
//-----------------------------------------------------------------------------


//-----------------------------------------------------------------------------
// Changelog
// 1.8
// - now ignoring elements with style {display: none;}
// - add local version of GM_getValue and GM_setValue

// 1.71
// - Adoption for org.
// 1.7
// - internal optimizations regarding performance (many thanks to Finargol for pointing in right direction)
//
// 1.6
// - now displaying <input> and <textarea> tag texts and images
// - added ignore/don't display handling for bunch of html tags (which are probably not used by wod, but just to be safe)
//
// 1.5
// - now displaying selected option inside <select> tag
//
// 1.4
// - label instead of span by the checkboxes
// - shortened all titles, english, french and croatian are ok, waiting for somebody who knows other languages to tell me if it is ok
// - changed internal representation of localized strings to ease maintenance
// - internal reorganization
// - moved "BBCode create" button to the bottom of central part of the page (it confused some other scripts when placed on top, plus some users said it doesn't suit them when placed on top)
// - added encodeuri to url handling to handle international characters in uris
// - added Finargol to contributor list (thanks for useful input and testing on french server)
//
// 1.3
// - included french translation and allowed all wod sites to use since should not depend on language used.
// - added some translations (based on Google translate, corrections most welcome!!!)
// - changed place where button and options are located to be consistent in popup pages where menu tree on left does not exist
// - now handling urls without href
// - fixed some minor formatting issues (newlines and tabs inside text)
//
// 1.2
// - included font color and size in item, hero, group, monster, etc tags
// - fixed problem with forum post ids
// - added handling for monuments
// - after code is created page is positioned at the beginning of created bbcode
// - created BBCode placed inside text area box for easier copying
//
// 1.1 
// - changed how font size, family and size are handled
// - added checkboxes so user can decide whether to include font size, family and size into BBCode created (plain text works better with various skins)
// - added anonymous function around code so not to polute, or interact with, global namespace
//
// 1.0 
// - initial release
//-----------------------------------------------------------------------------
