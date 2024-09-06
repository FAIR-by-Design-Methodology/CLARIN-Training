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

[Download the slides here](https://github.com/FAIR-by-Design-Methodology/IDCC24workshop/raw/main/resources/02%20Skills4EOSC/Skills4EOSC-IDCCworkshop_FAIR-by-Design_Methodology.pptx){:download}


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

!!! tip "Final Tips"

    - **Maintain a Consistent Style**: Use consistent image sizes, captions, and positioning throughout your content.
    - **Test Compatibility**: Ensure that the multimedia elements work in the Markdown processor or platform you’re using.
    - **Responsive Design**: Ensure that your multimedia content is responsive, especially when using HTML, so that it looks good on different screen sizes.
    - **Provide Download Links for Media**: Some users might prefer or need to download media files instead of viewing them directly in the browser.

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

??? warning Don’t Ignore Accessibility

	- Why: Multimedia content should be accessible to all users, including those with disabilities.
	- Tip: Use alt text, provide transcripts for videos, and ensure that interactive elements are keyboard-navigable.

??? warning	"Don’t Link to Unreliable External Sources"

	- Why: Linking to external media that may be removed or blocked can result in broken links or missing content.
	- Tip: Host essential media content yourself or ensure that external links are stable.
	
??? warning	"Don’t Use Auto-Playing Media"

	- Why: Auto-playing videos or audio can be intrusive and may disrupt the user’s experience.
	- Tip: Always allow users to control when media plays.

??? warning Don’t Neglect to Credit Sources"

	- Why: Failing to attribute media to its original creator can lead to copyright issues and diminish the trustworthiness of your content.
	- Tip: Always include proper citations or credits when using third-party media.

??? warning "Don’t Rely Solely on Multimedia"

	- Why: Some users may prefer or require text-based content, so always include a textual explanation or description of your multimedia.
	- Tip: Pair videos with summaries, and images with descriptive captions.

This approach helps create rich, multimedia-enhanced learning content that can cater to different learning modalities, making your materials more engaging and effective.


## Summary 



## Suggested Reading

- [Advanced editing in MD with multimedia](https://fair-by-design-methodology.github.io/FAIR-by-Design_ToT/latest/Stage%204%20%E2%80%93%20Produce/09-Content%20Development/09-Markdown%20Syntax/?h=video#videos)


