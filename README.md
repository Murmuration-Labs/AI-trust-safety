# AI Trust & Safety Explorations

*AI design pattern explorations for Trust &amp; Safety applications*

## Introduction

The rise of generative AI tools has brought about a new set of content abuse problems for the creators and services that create text, images, video, and audio content using artificial intelligence, and the platforms that host this content. 

While the underlying AI technology is relatively new, the discipline of Trust & Safety has developed over the years a wealth of knowledge and experience about identifying and mitigating risks related to problematic types of content. 

This document is intended to explore the application of Trust & Safety product thinking to a subset of the problems related to generative AI technology. It is not meant to be exhaustive, but it is intended to spark conversations about emerging best practices in the industry, to help make these tools safer, more trustworthy, and generally more aligned with user intentions.

## Emerging Industry Standards

Industry standards and best practices for handling generative AI content are still evolving. 

One significant effort to define the issues, and propose possible solutions comes from the [Partnership on AI](https://partnershiponai.org/)'s (PAI) [Responsible Practices for Synthetic Media](https://syntheticmedia.partnershiponai.org/#read_the_framework). It contains ideas for how different groups may apply responsible practices around AI generated content, including for: Builders of Technology and Infrastructure, Content Creators, and Distributors and Publishers.

One of the guiding principles of PAI's Framework includes disclosure about the use of generative AI, and we have chosen that principle to focus on in the explorations below. We believe there are many use cases where disclosure will be beneficial not just to content creators and distributors, but also to end users (readers) of content. 

- *For another discussion from 2021 regarding labeling of generative AI content, we also recommend [First Draft's article](https://firstdraftnews.org/long-form-article/from-deepfakes-to-tiktok-filters-how-do-you-label-ai-content/).*

# AI Blogging: Labeling AI-Assisted Text & Images

Blog posts and long-form articles on the web more generally, are one of the most common types of content online today. They usually consist of a combination of text and images, and sometimes embedded content such as a video, audio, or form. 

The design explorations below examine the most relevant points where a content creator, website owner, or platform provider might wish to disclose the presence and degree of AI assistance. They are:

- At the post preview level
- On the post itself (such as header/footer)
- Inline with the content 
- At the level of the feed
- On the user settings page

## Post Preview

Though each use case would need to be analyzed on its own, it seems that it would be beneficial to include some information about the use of generative AI at the level of a post preview, before a user clicks through to a post on a blog site. 

Here is a visualization for a possible design pattern to disclose the presence of AI-assistance, or AI-generated content, along with the estimated percent of AI-generated content in the post. 

![image](https://user-images.githubusercontent.com/72826716/222199496-2c615d54-8e5d-4a68-9cdb-fa5d4f12a6b0.png)

![image](https://user-images.githubusercontent.com/72826716/222199188-c5bc697e-08af-4acf-9b36-afe6e658f50e.png)

In the first example, we explored the idea that a blog post would be considered only "AI-assisted" where it contains a lower percentage of generative AI content (the blogger or platform would choose the threshold). 

In the second example, we propose using the label "AI-generated" where the content contains a higher percentage of generative AI content (also defined by the blogger or platform). 

Below is a variation where the "AI-assisted" tag or label appears in a pill-format:

![image](https://user-images.githubusercontent.com/72826716/222200223-41b16ba6-6ec1-4e25-84e0-823cbc875c87.png)

Tooltips may be used to convey more information about the tags or labels applied. 

Lastly, in the variation below, the presence of generative AI content is indicated by a more subtle robot emoji, which could be augmented by a tooltip that gives more information to the reader:

![image](https://user-images.githubusercontent.com/72826716/222200298-93ee546c-b74f-4e55-b510-afae8a3a0cad.png)

Though each use case would need to be analyzed on its own, it seems that it would be beneficial to include some information about the use of generative AI at the level of a post preview, before a user clicks through to a post on a blog site. 

## Post Level

The next obvious place to include responsible disclosure of the use of generative AI is at the level of a post or article itself. This might include elements in the footer, header, or sidebar. 

Here's an example visualization about how AI disclosure might work in the header of a blog post or web article:

![image](https://user-images.githubusercontent.com/72826716/222202749-fff97732-2eca-4630-b78a-c2cd2f7b261b.png)

In this example, there are three visual indicators:

* The text `AI-assisted` featured next the the length of the article
* The robot emoji
* A yellow banner indicating what percent of the content was generated by AI, along with a link to more information. 

And below is the accompanying visualization that might appear in the footer of this post or article, giving even more granular information about the AI technologies used. 

![image](https://user-images.githubusercontent.com/72826716/222203362-edb46088-4d8a-49ea-a0bb-9875351062c4.png)

In this case, we chose to display additional information about the models used for both text and graphical elements, and their relative percent use for the contents of the article. This metadata might also usefully link out to the AI/ML model cards for the models used, which would presumably contain more information. 

### Notes on determining AI content provenance: 

As this is only a visual/UI exploration, we have not resolved here the matter of *how* the information about the content's provenance (models used, etc.) might be determined. This is a separate and more technical problem, which might require some standardization on the part of generative AI tool providers, such that it becomes possible to export metadata about the content's origin which can effectively travel along with the data across other platforms. (See: [C2PA](https://en.wikipedia.org/wiki/C2PA) for parallel work in this direction)

Alternatively, if the blogging platform on which this article was posted itself includes generative tools as part of its editor, it may become relatively easy for the platform to track exactly which parts (and consequently the percentages) were AI generated, and which models were used. 

Lastly, it may become possible in the future to more accurately detect the presence of AI generated content by third party scanning applications, though there are legitimate concerns that will need to be addressed related to accuracy and cost before large scale scanning could become useful. 

## Inline Level

The next product surface where disclosure about the use of generative AI might occur would be at the inline level, displayed within or alongside the content itself. 

In this example, an AI generated image has a pill label, clicking on which might open up a box on the side with more details:

![image](https://user-images.githubusercontent.com/72826716/222207835-32c3486c-4e08-4c67-a9f9-92695612c18b.png)

Alternatively, we conceived of an "X-ray Mode" for blog post contents which when activated would automatically expand all the pertinent metadata about the use of generative AI tools. So in the example above, the user would not need to click the pill to expand the details section in the sidebar (it would already be open automatically).

Similarly, with X-ray Mode activated, there could be multiple ways of differentiating which part of text contents were generated by AI, as in the example below, which uses the color green to indicate AI-generated passages.

![image](https://user-images.githubusercontent.com/72826716/222208348-f624be7a-9195-4c30-97e8-fc25408b780d.png)

Other means of differentiating AI-text from human-written text that might be worth exploring: using a different font, a highlight color, or even a text or emoji symbol. We also have been exploring how one might use either custom markdown or markup for [annotating contributions by each party in a hybrid AI/human-written document](https://github.com/lost-books/AIMark-AI-attribution/). More experimentation needs to be done in this area.

## User Settings

In the examples above, we supposed that it would be possible and desirable for creators and/or platforms to disclose the presence and amount of generative AI contributions to a given piece of content, such as a blog post. 

The other side of that, then, would be enabling users or readers of the site to fine-tune their preferences for content that includes generative AI. Some users might want to exclude all such content from their browsing experience, while others might choose to allow only AI-assisted texts (between a certain threshold of AI contributions, and still others might be comfortable seeing posts that were fully AI-generated. 

Given that this is likely to be an important preference, we thought it would make sense to give two points of control to readers:

- At the feed level
- On the settings page. 

We imagined the feed level control might be something as simple as the following:

![image](https://user-images.githubusercontent.com/72826716/222250814-a79f62a2-918c-4294-a80b-e81f2c9cd409.png)

And then additional options and more information would be available in a dedicated section of the Settings page, as in the example below.

![image](https://user-images.githubusercontent.com/72826716/222251112-825c1ea9-881e-44b3-8565-c80f554174c1.png)

In this settings page example, we imagined having the following controls:

- Allow/disallow content with generative AI elements
- Set the threshold to include partial AI-assisted content or fully AI-generated content
- Show/hide labels for content that includes generative AI elements
- Enable X-ray view by default on all posts containing generative elements (readers could also toggle this individually on post pages)

Likely, as these technologies develop over time, both readers and creators will want to have other elements they can use to customize their experience related to generative AI content. 

# Conclusion

The above is just one exploration of UI design patterns for implementing responsible disclosure practices around generative AI use in blogging and online articles. It is our hope in sharing these examples to further the conversation around best practices and Trust & Safety in products making use of generative AI. We plan to produce some other case studies for other related tools, which we will publish here in the near future.

We welcome comments, questions, and more detailed conversations on these topics!

Thanks for reading.

## Credits

- Fernando Valverde: UI Design
- T. Boucher: Creative Direction, Writing
