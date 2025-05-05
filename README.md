# cop3504c-lab-10-meme-generator-solved
**TO GET THIS SOLUTION VISIT:** [COP3504C Lab 10: Meme Generator Solved](https://www.ankitcodinghub.com/product/cop3504c-lab-10-meme-generator-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;100436&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COP3504C  Lab 10: Meme Generator Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
Overview

In this lab, students will use an external library to create a meme generator library and executable. The purposes of this assignment is to give students practice with setting up, importing, using, and writing libraries in C++.

<strong>&nbsp;</strong>

<h2>SFML Setup</h2>
In this assignment, students will import and use <strong>SFML</strong> (Simple and Fast Multimedia Library). This section describes how to install SFML and integrate it into a project.

<h3>Installation</h3>
<ol>
<li><a href="https://www.sfml-dev.org/download/sfml/2.5.1/">Download</a> <strong>GCC 7.3.0 MinGW (SEH) – 64-bit</strong>; decompress into reasonable path (e.g., <strong>C:\Libraries</strong>).</li>
<li>Add path (e.g., <strong>C:\Libraries\SFML-2.5.1</strong>) as variable <strong>SFML_INSTALL</strong> to system variables.</li>
<li>Add binary path (e.g., <strong>C:\Libraries\SFML-2.5.1\bin</strong>) to <strong>PATH</strong> system variable.</li>
</ol>
&nbsp;

<h3>Integration</h3>
Under the compiler settings, add the following lines to your CMakeLists.txt to integrate SFML into the project:

<strong>set(</strong><strong>SFML_DIR</strong><strong> “</strong><strong>C:/Libraries/SFML-2.5.1/lib/cmake/SFML</strong><strong>“) find_package(</strong><strong>SFML 2.5 COMPONENTS graphics audio REQUIRED</strong><strong>) </strong>

&nbsp;

You can add the library to your <strong>memer</strong> library target by specifying link instructions:

<strong>add_library(</strong><strong>memer memer.cpp</strong><strong>) target_link_libraries(</strong><strong>memer sfml-graphics sfml-audio</strong><strong>) </strong>

&nbsp;

Likewise, you can link your <strong>memer</strong> library to your <strong>memeify</strong> executable:

<strong>add_executable (</strong><strong>memeify memeify.cpp</strong><strong>) target_link_libraries(</strong><strong>memeify memer sfml-graphics sfml-audio</strong><strong>) </strong>

&nbsp;

<h3>Use</h3>
To use SFML, you simply include the appropriate header in your code and use SFML constructs in your project:

<strong>#include</strong> <strong>&lt;SFML/Graphics.hpp&gt;</strong>

&nbsp;

The <strong>Cave-Story.ttf</strong> open-source font file has also been provided for this project.

&nbsp;

<u>Classes</u>

There are a few important classes that you will want to read about in the SFML documentation.

&nbsp;

<em>sf</em><em>::</em>Image

This object is an image in system memory (RAM), stored as a series of pixels.

&nbsp;

<em>sf</em><em>::</em>Texture

This object represents a read-only version of image data pre-formatted and stored in video memory (VRAM).

&nbsp;

<em>sf</em><em>::</em>Font

A font for use in SFML routines. Typically loaded from a file.

&nbsp;

<em>sf</em><em>::</em>String

The SFML native String format.

<em>&nbsp;sf</em><em>::</em>Sprite

A drawable class; it references a section of a texture that is used for display / drawing.

&nbsp;

<em>sf</em><em>::</em>Text

A drawable text element; incorporates a Font and a String. Positioning can be set as needed.

&nbsp;

<em>sf</em><em>::</em>RenderTexture

A read-write texture; data is stored in video memory. This object can be drawn on.

&nbsp;

<h2>Specification</h2>
In this assignment, students will generate two artifacts, a memer library and a memeify executable.

&nbsp;

<h3>Library</h3>
The library will be named <strong>memer</strong>. It should incorporate the function below and include <strong>memer.h</strong>:

<em>sf</em><em>::</em>Image<strong> generateMeme(</strong><em>sf</em><em>::</em>Image base, <em>sf</em><em>::</em>String topText, <em>sf</em><em>::</em>String bottomText <strong>= “”</strong>,&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; int topX <strong>= -1</strong>, int topY <strong>= -1</strong>, int bottomX <strong>= -1</strong>, int bottomY <strong>= -1</strong>)

&nbsp;

Takes in an base to be used as the base image. Returns a new <em>sf</em><em>::</em>Image with <strong>topText</strong> drawn over it at location (<strong>topX</strong>, <strong>topY</strong>) in the provided font. If no coordinates are provided, <strong>topText</strong> should be centered horizontally and be 1/3 from the top of the image. If it is provided, <strong>bottomText</strong> is drawn at location (<strong>bottomX</strong>, <strong>bottomY</strong>). If provided, the t<strong>bottomText</strong> should be placed 1/3 from the bottom of the image.

&nbsp;

<u>In general, adding text to an image will consist of the following steps:</u>

<ol>
<li>Converting the <strong>Image</strong> into a <strong>Texture</strong></li>
<li>Wrapping the <strong>Texture</strong> in a <strong>Sprite</strong></li>
<li>Drawing the <strong>Sprite</strong> on a fresh &amp; empty <strong>RenderTexture</strong></li>
<li>Loading a <strong>Font</strong>, and using it to construct a <strong>Text</strong> element</li>
<li>Drawing the <strong>Text</strong> on the <strong>RenderTexture</strong></li>
<li>Extracting an <strong>Image</strong> from a <strong>Texture</strong>, derived from the <strong>RenderTexture</strong>.</li>
</ol>
&nbsp;

<strong><u>NOTE</u></strong>: graphics are traditionally done differently in 2D and 3D, resulting in the Image from a Texture being upside down; make sure to flip it horizontally before returning it!

&nbsp;

&nbsp;

<h3>Executable</h3>
Executable should function with just file &amp; top text: … but should also accept a partial / full complement:

<table width="687">
<tbody>
<tr>
<td width="343">&nbsp;

<table width="335">
<tbody>
<tr>
<td width="335"><strong>finn@BMO</strong><strong>:</strong><strong>~</strong><strong>$ ./</strong><strong>memeify doge.jpg “Such memes” </strong></td>
</tr>
</tbody>
</table>
</td>
<td width="343">&nbsp;

<table width="335">
<tbody>
<tr>
<td width="335"><strong>finn@BMO</strong><strong>:</strong><strong>~</strong><strong>$ ./</strong><strong>memeify doge.jpg “Such memes”\ </strong><strong>&gt; </strong><strong>“wow” 360 90 120 360 </strong></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>
&nbsp;

&nbsp;

&nbsp;

The executable should 1) display the image in a window until the window is closed, and 2) save the image with a new name based on the old one in the form of <strong>STEM-meme.EXT</strong>; e.g., if the original image was “<strong>doge.jpg</strong>”, the new image saved should be “<strong>doge-meme.jpg</strong>”.

&nbsp;

<h2>Submissions</h2>
<strong>NOTE</strong>: Your output must match the example output *exactly*. If it does not, <strong><em>you will not receive full credit for your submission</em></strong>! (Note that matching sample output is necessary, but not sufficient, for full credit.)

&nbsp;

Files: memeify.zip

Method: Submit on Canvas

&nbsp;

<h3>Compressed Archive (memeify.zip)</h3>
We do not list required source files, only headers. You should include additional source or header files in addition to those listed – based on your design – but you must have the listed files at a minimum.

&nbsp;

Your compressed file should have the following directory/file structure:

&nbsp;

memeify.zip&nbsp; &nbsp;&nbsp; &nbsp; memeify (directory)

CMakeLists.txt&nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp; memer.h

(Other sources / folders)

&nbsp;

&nbsp;
