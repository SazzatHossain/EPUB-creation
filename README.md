# EPUB CREATION DOCUMENTATION

This README documentation explains whatever steps are necessary to convert, create a epub ebook from a docx file.

This document cover the following topics:
1. [Software Required](#softwares)
2. [Supported File Formats](#suported_formats)
3. [Convert Main File](#main_file_conversion)
4. [Import File to Calibre](#import_to_cailbre)
5. [Convert File to EPUB](#convert_to_epub)
6. [Editing](#edit_file)
7. [Import Image](#image_import)
6. [Image Responsive](#image_responsive)
7. [Convert File again after Image Upload](#convert_again)

## <a name="#softwares">Software Required</a>
* (Download link:[Calibre] (https://calibre-ebook.com/download_windows64 “Calibre”) 
    <p>or</p>                  
* (Download link:[Sigil] (https://www.techspot.com/downloads/downloadnow/5797/?evp=05a807ccbb500373c0b99755dbd3a88c&file=1 “Sigil”)

We will use Calibre because it has much more functionality than sigil.

## <a name="suported_formats">Supported File Formats</a>
* Input formats accepted: AZW, CBC, CBR, CBZ, ePUB, FB2, HTM, HTML, LIT, LRF, MOBI, ODT, OPF, RB, PDB, PDF, PML, PMLZ, PRC, RECIPE, RTF, SHTM, SHTML, TCR, TXT, XHTM, XHTML, DOC, DOCX.
* Output formats available: EPUB, LIT, LRF, FB2, MOBI, PDB, PDF, PMLZ, RB, TCR, TXT.

 ## <a name="main_file_conversion">Convert Main File</a>

First open the file with Microsoft Word(Above 2010 recommended). If the file is in DOCX format we do not have to follow this step. If this is in doc or other format we should save the file with the docx format extention. It will be easy to import and work on calibre if the file format is docx. **We should avoid PDF file cause it is not suitable format to make epub ebook.**

## <a name="import_to_calibre">Import File to Calibre</a>
* Open calibre Application.
* Click On **Add books** option.
* Go to the directory on the doc/docx file which we want make an EPUB ebook.
* Select the file and open it.

## <a name="convert_to_epub">Convert File to EPUB</a>
 Before editing the file we must have to convert it into a ebook format. We should convert this file to EPUB through the following steps:
 
 * First select the book we uploaded.
 * The click on the **Convert books** option.
 * A new pop-up window will open. There are many options and many things we can do here. But we will simply fill up the options on the right seleting the metadata option. We can also add a **Book cover** from the left section.
 * After completing these steps check the Output format option from the top-right corner. If it is already selected to EPUB format then click the ok button from bottom-right corner to convert it to EPUB.
 
## <a name="edit_file">EDITING</a>
After successfully convert the file to EPUB we can now edit/modify the EPUB file. To modify the epub file with calibre we should follow the following rules:

* Put the mouse cursor on the converted EPUB or select the epub and put the mouse cursor on the option shown in below image.
* Right click on it and click on Edit book option.
* A new window will open. It's the calibre editor. We can easily modify or create new epub book with this editor.

Lets go through the option of the editor. There are many option in the editor but we will go through the option we might need.
EPUB is basically written in xhtml. So basic html and css idea is needed to edit a EPUB file.

See through the left option of the editor.
* **Title Page:** Title page means the cover page of the book. If we upload a cover page before when we converted the file then the cover page link will be shown here. We can modify the title page from here.
* **index.html:** The index.html is the main file where the ebook's content are in. It is written in html and styled with css. We can edit out content through these file.
* **Styles:** The text section have the stylesheets means the css file for styling the contents.
* **Images:** The images section are for all the image contents which we will upload and use in our ebook.
* **Fonts:** Font section contains all the font we will use in this EPUB. 

## <a name="image_import">Import Image</a>

If we want to add images in the epub we can upload and add the images through the following steps:

* First click on the **'+'** option from the top-left corner shown below.
* A pop-up will open. From here click on the **Import resource file(image/font/etc.)** option.
* Navigate and select the image you want to upload. Click open.
* Then click the **OK** option from the pop-up menu. See the Images directory from the left options whether the images has been uploaded or not.

We can use this image in our epub through html **img** tag. We also can upload fonts through this process if we want.

## <a name="image_responsive">Images Responsive</a>

The images we uploaded will not be responsive. So we have to make it responsive. Fist check the  img tag from **index.html** file and see there is already a classname given by **calibre.** Or manually add image with **img** tag and give a classname.
Let the image classname be **"calibre-image"**

* Open the **stylesheet.css** file. 
* Write **".calibre-image{ }"**
* Inside the curly braces write following css properties and values like below:
    * height: auto;
    * width: 100%;
    * margin: 0;
    * padding: 0;
By this the images will be responsive. Name all the images classname same. Then it will be applied to all the images.

## <a name="convert_again">Convert File again after Image Upload</a>
 
 After adding images the epub file size will be larger. So we have to convert it again to EPUB format to reduce size.
 We should follow the old step to convert this file again to EPUB.