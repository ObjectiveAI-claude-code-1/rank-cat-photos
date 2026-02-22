# rank-cat-photos

A sophisticated ObjectiveAI vector function for ranking cat photographs based on multiple dimensions of visual and emotional quality.

## Overview

The `rank-cat-photos` function evaluates and ranks cat photographs to identify which images most effectively combine genuine charm, artistic excellence, and technical quality. Rather than relying on single criteria, this function integrates evaluations across multiple dimensions to produce a comprehensive ranking that respects both the artistry of photography and the authentic nature of feline subjects.

## Input

The function accepts an array of cat photo objects. Each photo must include:

- **url** (required): The URL or file path to the cat photo image
- **title** (optional): A descriptive title or label for the photo
- **photographer** (optional): Credit to the photographer

The input array must contain between 2 and 100 photos.

### Example Input

```json
[
  {
    "url": "https://example.com/photo1.jpg",
    "title": "Curious Kitten in Sunlight",
    "photographer": "Jane Smith"
  },
  {
    "url": "https://example.com/photo2.jpg",
    "title": "Sleepy Cat on Cushion",
    "photographer": "John Doe"
  },
  {
    "url": "https://example.com/photo3.jpg",
    "title": "Playful Tabby"
  }
]
```

## Output

The function returns an array of numerical scores that rank the input photos from highest to lowest quality. The scores are normalized so they sum to 1, with higher scores indicating photos that better exemplify excellent cat photography across all evaluated dimensions.

### Example Output

```json
[0.42, 0.35, 0.23]
```

In this example, the first photo receives the highest score (0.42), the second photo receives a strong score (0.35), and the third photo receives the lowest score (0.23). These scores reflect the relative ranking of the photos based on the complete evaluation.

## What It Evaluates

The `rank-cat-photos` function evaluates photos across four core dimensions:

### 1. Charm and Authenticity

The function assesses whether each photo captures genuine feline personality and authentic moments. It evaluates:
- The emotional resonance and appeal of the subject
- Whether the cat displays natural behavior or seems posed
- The emotional connection the image creates with viewers
- Real moments of affection, playfulness, curiosity, or characteristic behavior

Photos showing unguarded, authentic moments of the cat's true nature rank higher than those appearing staged or awkwardly posed.

### 2. Compositional Excellence

The function evaluates the photographer's artistic choices and visual arrangement. It assesses:
- Framing and angle selection
- Visual balance and use of space
- Meaningful positioning of the cat within the frame
- Whether the background complements or detracts from the subject
- Overall intentionality and creative vision

Photos with thoughtful, purposeful composition that enhances the presentation of the subject rank higher than those with careless or haphazard arrangement.

### 3. Visual Clarity and Technical Quality

The function evaluates the technical soundness of each image. It assesses:
- Sharpness and focus on the cat
- Quality and appropriateness of lighting that reveals detail and texture
- Clarity and visibility of fine details
- Accuracy of color reproduction

Technically sound photographs that are in focus with proper lighting allow full appreciation of the subject and rank higher than images with poor focus, inadequate lighting, or unclear details.

### 4. Authentic Moment Capture

The function evaluates whether the photo captures a genuine slice of feline life. It assesses:
- Spontaneity and naturalness versus staged arrangement
- Honoring of the cat's authentic nature and behavior
- Narrative quality and story-telling power
- Alignment with how cats naturally behave

Photographs capturing unguarded moments that reveal true feline character and behavior rank higher than artificially posed images.

## Use Cases

### 1. Social Media Curation
Social media platforms can use this function to automatically identify the best cat photos from user submissions, surfacing top-ranked images to the homepage, featured collections, or trending sections.

### 2. Photography Contests
Photography competitions can employ this function to assist in the selection process, identifying top-tier submissions that demonstrate excellence across multiple dimensions of quality.

### 3. Content Publishing
News organizations, blogs, and content creators can use this function to select the most captivating cat photographs to accompany articles or stories about cats.

### 4. Personal Photo Library Organization
Cat enthusiasts can use this function to organize and discover their best cat photographs, automatically identifying favorite moments and arranging their libraries by quality.

### 5. E-Commerce and Marketplace
Online pet retailers or cat-focused marketplaces can use this function to rank product images, testimonial photos, or user-generated content featuring cats.

### 6. Automated Image Review
Automated systems for processing large volumes of cat photos (such as rescue organizations or shelters cataloging animals) can use this function to identify the most photogenic and appealing images of each animal.

## Technical Details

The `rank-cat-photos` function employs a multi-task evaluation approach that combines specialized sub-functions for optimal accuracy.

### Sub-Functions

The ranking is produced by integrating evaluations from the following specialized sub-functions:

- **Rank by Charm and Authenticity**: https://github.com/ObjectiveAI-claude-code-1/score-cat-authenticity
  Compares all photos to identify which most effectively capture genuine personality and authentic moments.

- **Rank by Compositional Excellence**: https://github.com/ObjectiveAI-claude-code-1/rank-cat-composition
  Compares all photos to identify which demonstrate superior artistic choices in framing, angle, balance, and space utilization.

- **Score by Visual Clarity**: https://github.com/ObjectiveAI-claude-code-1/score-cat-photo-quality
  Evaluates each individual photo for technical quality including focus sharpness, lighting quality, detail clarity, and color accuracy.

These sub-functions work in concert, with their individual outputs combined into the final ranking. The function's philosophy values both the technical craft of photography and respect for authentic feline moments, ensuring that excellence in all dimensions is recognized and rewarded.

## Design Philosophy

The `rank-cat-photos` function reflects a philosophy that:

- **Respects Authenticity**: Photos that capture genuine feline moments rank higher than those that feel artificially posed or manipulated
- **Values Artistry**: Intentional composition and creative vision are recognized alongside technical excellence
- **Balances Multiple Dimensions**: Excellence across multiple criteria is valued more highly than exceptional performance in a single area
- **Celebrates Feline Nature**: The function honors the spontaneity, personality, and natural behavior of cats as subjects
- **Appreciates Connection**: Photos that create emotional resonance and connection with viewers are recognized and rewarded

## Implementation

This is an ObjectiveAI vector function that accepts an array of photos as input and produces a normalized array of scores summing to approximately 1.0. The function integrates evaluations from multiple specialized sub-functions that each contribute expertise in different aspects of photo quality assessment.