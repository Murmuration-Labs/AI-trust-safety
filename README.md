# AI Trust & Safety Explorations

*AI design pattern explorations for Trust &amp; Safety applications*

## Introduction

The rise of generative AI tools has brought about a new set of content abuse problems for the services that create text, images, video, and audio content using artificial intelligence, and the platforms that host this content. 

While the underlying AI technology is relatively new, the discipline of Trust & Safety has developed over the years a wealth of knowledge and experience about identifying and mitigating risks related to problematic types of content. 

This document is intended to explore the application of Trust & Safety product thinking to a subset of the problems related to generative AI technology. It is not meant to be exhaustive, but it is intended to spark conversations about emerging best practices in the industry, to help make these tools safer, more trustworthy, and generally more aligned with user intentions.

## Emerging Industry Standards

Industry standards and best practices for handling generative AI content are still evolving. 

One significant effort to define the issues, and propose possible solutions comes from the [Partnership on AI](https://partnershiponai.org/)'s (PAI) [Responsible Practices for Synthetic Media](https://syntheticmedia.partnershiponai.org/#read_the_framework). It contains ideas for how different groups may apply responsible practices around AI generated content, including for: Builders of Technology and Infrastructure, Content Creators, and Distributors and Publishers.

One of the guiding principles of PAI's Framework includes disclosure about the use of generative AI, and we have chosen that principle to focus on in the explorations below. We believe there are many use cases where disclosure will be beneficial not just to content creators and distributors, but also to end users (readers) of content. 

## AI Blogging: Labeling AI-Assisted Text & Images

Blog posts and long-form articles on the web more generally, are one of the most common types of content online today. They usually consist of a combination of text and images, and sometimes embedded content such as a video, audio, or form. 

The design explorations below examine the most relevant points where a content creator, website owner, or platform provider might wish to disclose the presence and degree of AI assistance. They are:

- At the post preview level
- On the post itself (such as header/footer)
- Inline with the content 
- At the level of the feed
- On the user settings page

### Post Preview

Though each use case would need to be analyzed on its own, it seems that it would be beneficial to include some information about the use of generative AI at the level of a post preview, before a user clicks through to a post on a blog site. 

Here is a visualization for a possible design pattern to disclose the presence of AI-assistance, or AI-generated content, along with the estimated percent of AI-generated content in the post. 

![image](https://user-images.githubusercontent.com/72826716/222199496-2c615d54-8e5d-4a68-9cdb-fa5d4f12a6b0.png)

![image](https://user-images.githubusercontent.com/72826716/222199188-c5bc697e-08af-4acf-9b36-afe6e658f50e.png)

In the first example, we explored the idea that a blog post would be considered only "AI-assisted" where it contains a lower percentage of generative AI content (the blogger or platform would choose the threshold). 

In the second example, we propose using the label "AI-generated" where the content contains a higher percentage of generative AI content (also defined by the blogger or platform). 

Below is a variation where the "AI-assisted" tag or label appears in a pill-format:

![image](https://user-images.githubusercontent.com/72826716/221923628-15b2e96f-5d04-483b-95ca-6e6ccc6632a1.png)

Lastly, in the variation below, the presence of generative AI content is indicated by a more subtle robot emoji, which could be augmented by a tooltip that gives more information to the reader:

![image](https://user-images.githubusercontent.com/72826716/221924801-a254bc4e-b529-460c-8f5b-b856107fa199.png)
