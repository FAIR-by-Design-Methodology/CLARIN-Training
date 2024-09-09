---
title: "Rich learning experience"
author: "Skills4EOSC"
tags: 
    - Multimedia
    - Learning modality
    - Accessibility
---

# Rich learning experience

## Slides

[Download the slides here](https://github.com/FAIR-by-Design-Methodology/CLARIN-Training/raw/main/resources/1st%20Session/06%20Rich%20learning%20exp/Rich_learning_exp.pptx){:download}


## Learning objectives

- identify different learning modalities
- design multimedia rich content
- develop accessible learning content

## Learning modalities

Effective learning experience is crucial for application of the obtained knowledge and skills in real world context. To achieve this, not only the learning objectives, but all content, activities, assignments and assessments must be learner-centered.

Learners perform best when they are engaged in authentic activities, collaborate with peers to share and deepen their understanding, and apply their existing skills to different contexts and new problems.

Rich learning experiences can be supported by

- inquiry-based learning structures, such as projects and performance tasks
- thoughtfully interwoven direct instruction
- opportunities to practice and apply learning

It is important that learners are given meaningful tasks that build on their prior knowledge together with a safe positive environment in which they can receive timely and helpful feedback.

Units should be well structured so as to reduce the unnecessary cognitive load, and based on multiple modalities and tools for accessing information and expressing learning to support different types of learners.

Learning modalities refer to the different ways individuals process and retain information. These modalities highlight the diverse preferences and strengths people have when it comes to learning. The most commonly recognized learning modalities include:

!!! tip	"Visual"

    Learners who prefer visual modalities understand and remember information better when it is presented in a visual format, such as diagrams, charts, graphs, and images. They benefit from seeing concepts and ideas.
	
!!! tip "Auditory"

    Auditory learners process information most effectively when it is heard. They learn well through lectures, discussions, podcasts, and verbal instructions.
	
!!! tip "Reading/Writing"

    These learners prefer interacting with text-based information. They excel in reading and writing tasks, such as taking notes, reading books, and writing essays or reports.
	
!!! tip "Kinesthetic"

    Kinesthetic learners are hands-on learners who grasp concepts best through physical activity and movement. They benefit from experiments, role-playing, and using objects or tools.

Some theories and frameworks expand on learning modalities, recognizing that people often use a combination of these modalities rather than relying on a single one. Understanding and catering to different learning modalities can enhance teaching strategies and improve learning outcomes by providing varied methods of instruction that align with learners’ preferences.

## Adding multimedia to the learning content

Incorporating multimedia into learning content is directly related to learning modalities because it allows educators to address and engage different types of learners more effectively. Multimedia aligns with various learning modalities:

1. Visual Learners: Multimedia can include videos, infographics, animations, and diagrams that visually represent concepts. This appeals to visual learners by providing clear and engaging ways to understand and remember information.
2. Auditory Learners: By adding audio elements such as narrations, podcasts, or sound effects, multimedia caters to auditory learners who benefit from hearing information. This can include explanations, discussions, or even background music that reinforces the learning material.
3. Reading/Writing Learners: Multimedia can integrate text-based elements, such as subtitles, captions, or interactive reading materials, which appeal to learners who prefer to read and write. Hyperlinks to additional reading, digital flashcards, or interactive eBooks also support this modality.
4. Kinesthetic Learners: Interactive multimedia, such as simulations, virtual labs, or drag-and-drop activities, allows kinesthetic learners to engage with the content through physical interaction. This hands-on approach helps them better grasp and retain the material.

By integrating multimedia, educators can create a richer, more inclusive learning environment that accommodates different learning preferences. It also helps to reinforce concepts through multiple channels, increasing the likelihood that learners will understand and retain the material.

### Adding multimedia to MD content

While Markdown itself is quite simple, it can be enhanced with multimedia by incorporating various elements such as images, videos, audio, and interactive content. Different types of multimedia can be added to Markdown content by:

#### Images

To add images, use the following syntax:

    ![Alt text](image-url)

such as
```
    ![A beautiful sunset](https://example.com/sunset.jpg)
```
or if it is a local file 
```
    ![Alt text](./path/to/image.jpg)
```
!!! tip "Images in MD"

    One of the most important things to remember is that the "alt text" is alternative text for the image that is used for accessibility purposes. It will be read by a screen reader that helps learners with visual impairments.

Icons add visual interest and can help convey meaning quickly. While Markdown itself doesn’t support icons natively, you can use HTML or rely on Markdown extensions or themes that support icons.

- Example
```
    <i class="fas fa-info-circle"></i> This is an informational icon.
```

#### Videos

While Markdown doesn’t natively support embedding videos, you can use HTML to embed videos from platforms like YouTube or use a link to direct users to the video.

- Using HTML (embedded video):
```
    <iframe width="560" height="315" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allowfullscreen></iframe>
```
- Using a link (linked video):
```
    [Watch this video](https://www.youtube.com/watch?v=dQw4w9WgXcQ)
```
!!! tip "Videos in MD"

    As in the examples, it is best practice to put the video on a video streaming provider and then link or embed it. This helps keep the repo lean as video files are quite big, plus it allows you to use some advanced features such as auto captioning, chapters, playlists, etc.

#### GIFs

Another option is to use embedded GIFs as short videos.

In this case it is as if you are adding an image

    ![Funny cat](https://example.com/funny-cat.gif)

#### Audio

To include audio, you can also use HTML:

    <audio controls>
        <source src="audio-file-url.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
    </audio>

- for an example

    <audio controls>
        <source src="https://example.com/audio.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
    </audio>

!!! warning "Accessible multimedia"

    Provide transcripts and captions for audio and video content to make them accessible to all users.

#### Interactive elements

For more complex interactive elements, one might use HTML or specialized tools that support enhanced Markdown (like Jupyter notebooks or MkDocs):

- Interactive Maps, Charts, or Widgets: You can embed these by using ```<iframe>``` or specific Markdown extensions supported by your platform.

- Example (Embedded Map using HTML)
```
    <iframe src="https://www.google.com/maps/embed?pb=!1m18..." width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
```
#### Slideshows

If you need to add a slideshow, you might use Markdown libraries such as Reveal.js that convert Markdown into presentation slides.

#### Linking to Files

For documents, PDFs, or other files:
```
    [Download the PDF](https://example.com/document.pdf)
```
#### Markdown Extensions

Some Markdown processors support extended syntax for including multimedia, such as MathJax for equations or Mermaid for diagrams.

See the example in the previous module where the structure is presented using Mermaid. 

Admonitions are special call-out boxes that highlight important information or warnings. They help users quickly identify key points or notes. Use Admonitions to Highlight Key Information.

Code blocks can also be used to provide source code examples to learners.

Integrating Jupyter Notebooks with MkDocs can provide a powerful way to combine interactive code, data analysis, and documentation. This is particularly useful for projects that involve both technical explanations and live code examples. To mix MD with Jupyter Notebooks you can:

- Convert Jupyter Notebooks to Markdown or HTML
    - Jupyter Notebooks can be converted to Markdown or HTML, which can then be included in your MkDocs site.
- Use nbviewer or GitHub Gists for Live Notebooks
    - services like nbviewer or GitHub Gists to embed live notebooks, such as

```
    [View Jupyter Notebook](https://nbviewer.jupyter.org/github/username/repository/blob/main/notebook.ipynb)
```

- Use jupyter-book for a Comprehensive Solution
    - consider using jupyter-book, which is designed to work with Jupyter Notebooks and Markdown to create interactive books.
    - also, the jupyter-mkdocs plugin enables you to run Jupyter Notebooks directly within MkDocs.

!!! tip "Final Tips"

    - **Maintain a Consistent Style**: Use consistent image sizes, captions, and positioning throughout your content.
    - **Test Compatibility**: Ensure that the multimedia elements work in the Markdown processor or platform you’re using.
    - **Responsive Design**: Ensure that your multimedia content is responsive, especially when using HTML, so that it looks good on different screen sizes.
    - **Provide Download Links for Media**: Some users might prefer or need to download media files instead of viewing them directly in the browser.
    - **Documentation**: Ensure that you provide clear documentation and context for users interacting with the Jupyter notebooks.

### DON'T

??? warning	"Don’t Overload Pages with Too Much Multimedia"

    - Why: Excessive multimedia can overwhelm users, slow down page loading, and distract from the core content.
	- Tip: Use multimedia sparingly and only when it adds value to the content.

??? warning	"Don’t Use Low-Quality Media"

	- Why: Poor-quality images, videos, or audio can reduce the credibility and professionalism of your content.
	- Tip: Always use high-resolution images and clear audio/video files.

??? warning "Don’t Forget to Test Media Content"

	- Why: Media might not display or function as expected across different browsers or devices.
	- Tip: Always test embedded media on multiple platforms before publishing.

??? warning "Don’t Ignore Accessibility"

	- Why: Multimedia content should be accessible to all users, including those with disabilities.
	- Tip: Use alt text, provide transcripts for videos, and ensure that interactive elements are keyboard-navigable.

??? warning	"Don’t Link to Unreliable External Sources"

	- Why: Linking to external media that may be removed or blocked can result in broken links or missing content.
	- Tip: Host essential media content yourself or ensure that external links are stable.
	
??? warning	"Don’t Use Auto-Playing Media"

	- Why: Auto-playing videos or audio can be intrusive and may disrupt the user’s experience.
	- Tip: Always allow users to control when media plays.

??? warning "Don’t Neglect to Credit Sources"

	- Why: Failing to attribute media to its original creator can lead to copyright issues and diminish the trustworthiness of your content.
	- Tip: Always include proper citations or credits when using third-party media.

??? warning "Don’t Rely Solely on Multimedia"

	- Why: Some users may prefer or require text-based content, so always include a textual explanation or description of your multimedia.
	- Tip: Pair videos with summaries, and images with descriptive captions.

This approach helps create rich, multimedia-enhanced learning content that can cater to different learning modalities, making your materials more engaging and effective.

## Accessibility

All developed learning content should be accessible to a wide range of learners with different needs from a variety of backgrounds, abilities and learning styles. To ensure this the developed content needs to be checked so that access is optimised and all unnecessary barriers are removed making it inclusive and easier to engage with by all learners including people with disabilities.

Accessible educational materials (AEM) are defined as educational materials that are designed or later enhanced in such a way that it makes them usable across the widest range of learner variability. For digital learning materials and technologies this means that they are accessible if they can be easily used by anyone, including people with disabilities. Accessible digital learning materials need to be designed so that they can be directly used without assistive technology or made usable with assistive technology. 

These are just a few examples that illustrate the need for accessible materials:

- simple text structure helps learners with a variety of learning needs, including learners for whom the language used is not their native language
- simple navigation through the materials should help access the content from mobile devices, as well as learners with low vision
- adding captions to videos helps learners with hearing impairment as well as learners that have low prior knowledge on the subject and key terminology.

### General guidelines for development of accessible materials

Most of the techniques used for development of accessible learning materials are based on the Universal Design for Learning (UDL) that focuses on the design of learning materials that are aimed to be inclusive of as many learners as possible. This approach, combined with the assistive and accessible technologies, can ensure that every learner has access to the same materials. 

UDL is based on three fundamental principles:

1. **Multiple means of representation**
	- learning content should be presented in different ways and formats
2. **Multiple means of action and expression**
	- several options for action and expression should support the demonstration of acquired knowledge
3. **Multiple means of engagement**
	- learners differ in what engages and motivates them so multiple options should be provided

The following are some general tips and guidelines that should help develop accessible learning content:

!!! tip "Present the information in multiple ways and formats"

    This helps support various learning styles and provides alternatives for different impairments.

!!! tip "Use simple language"

    The materials should be accessible for the learners' varying levels of access, background, and ability.
	An option is to provide additional resources to support learners that have comprehension difficulties.

!!! tip "Use headings"

    Assistive technologies differentiate the structural elements in the text (body text and different levels of headings). These help screen readers process the text correctly.

!!! tip "Use table of content"

    Helps learners navigate to the required information easily.

!!! tip "Provide alternative text for images"

    The alternative text is read by the screen reader instead of the image. Decorative images should be marked as decorative so that the screen reader can skip them.

!!! tip "Use equation editors for math expressions"

    This format helps screen readers understand the content.

!!! tip "Use a high contrast color palette"

    High contrast supports learners with vision impairments.

!!! tip "Don't use color as the only way to convey information"

    Provide other alternative means for color blind learners.

!!! tip "Use descriptive links"

    Links to other documents should explain where the link is taking the learner.

!!! tip "Use tables only when required"

    If a table is truly the best way to convey the information and not just a layout trick, then use column and row headers to describe the content.

!!! tip "Provide closed captions and transcripts"

    Helps make the information in the video accessible to the vision impaired.

### Alternative text tips and tricks

For tip on how to write alternative text for images study the [Alternative text guide by WebAIM](https://webaim.org/techniques/alttext/). The key takeaways in the guide include:

- alternative text should be accurate and equivalent in representing content and function
- alternative text should be succinct
- alternative text should not be redundant
- alternative text should not include phrases such as "image of ..." or "graphic of ..."

Decorative images should have blank alternative text. A decorative image is an image that

- does not present important content
- is used for layout or non-informative purposes
- does not have a function (e.g. is not a link)

<div class="grid cards" markdown>

-   :material-human:{ .lg .middle } __Use accessibility evaluation tools!__

    ---

    Accessibility evaluation tools are not perfect. Even if they say that all is ok, it does not mean that your content is truly accessible. But they are a very good starting point.

    === "Slides"

        Use the integrated accessibility checker in Power Point:

        1. Open an existing presentation in PowerPoint and review the content. 
        2. Select the Review tab. 
        3. Select Check Accessibility.
        4. An Accessibility Checker pane will appear on the right with 'Inspection Results' displayed.

    === "Web content"

        Choose from the [Web Accessibility Evaluation Tools List](https://www.w3.org/WAI/test-evaluate/tools/list/) developed by W3C.

    === "PDF document"

        Check accessibility in Adobe Acrobat Pro.

        Open the PDF and then from the All tools menu on the left, select View more and then select Prepare for accessibility.

</div>

## Summary 

To create an engaging and inclusive learning experience, it’s essential to understand and integrate various learning modalities, incorporate multimedia effectively, and ensure accessibility. Learning modalities include visual, auditory, kinesthetic, and read/write styles, each catering to different ways individuals process information. By incorporating multimedia elements such as images, videos, audio, and interactive content, educators can address diverse learning preferences and enrich the educational experience. This not only helps in accommodating various learning styles but also makes the content more engaging and dynamic.

Ensuring accessibility is crucial in making learning resources usable for all individuals, including those with disabilities. This involves using descriptive alt text for images, providing transcripts and captions for audio and video content, and ensuring high color contrast and responsive design. Additionally, interactive elements should be navigable via keyboard, and semantic HTML should be employed to aid screen readers in interpreting content. By following these best practices, educational content becomes more inclusive, allowing all learners to access and benefit from the material effectively.

## Suggested Reading

- [Advanced editing in MD with multimedia](https://fair-by-design-methodology.github.io/FAIR-by-Design_ToT/latest/Stage%204%20%E2%80%93%20Produce/09-Content%20Development/09-Markdown%20Syntax/?h=video#videos)
- [More about accessibility and standards for accessibility](https://fair-by-design-methodology.github.io/FAIR-by-Design_ToT/latest/Stage%204%20%E2%80%93%20Produce/11-Accessibility/11-Checking_accessibility/)

