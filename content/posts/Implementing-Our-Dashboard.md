---
title: 'Implementing Our Dashboard'
summary: "Finishing backend implementation for the dashboard"
date: '2024-11-24T09:51:05-05:00'
draft: true
author: "Kerneep Sandhu"
# weight: 1 # pin post.
# aliases: ["/first"]
#tags: ["first"]
# cover:
#     image: "<image path/url>" # image path/url
#     alt: "<alt text>" # alt text
#     caption: "<text>" # display caption under cover
#     relative: false # when using page bundles set this to true
#     hidden: true # only hide on current single page
---

## 1. Week Overview
This week's goal was to finish the backend implementation for our dashboard, which provides the following functionality:
 - Navigate through uploaded files (by user), and AI-generated files.
 - Filter files based on tags (can select any number of tags).
 - Navigate through recently updated files and deleted files.

## 2. Achievements and Progress
- Key tasks and milestones completed:
  - Backend implementation for all dashboard functionality, except the `Upload` and `Create` buttons.
  - Testing coverage > 70% for `dashboard.py`.
  - **Milestone 1** completed!

## 3. Challenges Faced
- Description of major challenges encountered:
  - Was unclear on whether a file's url and thumbnail url needed to be unit tested.
- Impact of these challenges on the project:
  - Was having trouble with setting up `pytest fixtures` to create functional urls.

## 4. Solutions and Adjustments
- How challenges were addressed:
  - After discussion with Max, figured out that only confirmation needed for the urls would have to be the format. Testing the content accessed by the urls will need to be done in **Milestone 3**.
- Changes made to the project plan or methods:
  - Pytest fixtures only generate `ContentFile` and `GeneratedFile` models with completely fake data in `test_dashboard.py`.
  - Did not setup mock directories to create valid urls, since url for testing only needed to be a random string in the correct format.

## 5. Lessons Learned
- Verifying contents of files & thumbnails pointed to with the urls might be a challenge in the coming milestones.
- May need to push mock test files & thumbnail images to the repo for the above.

## 6. Next Week’s Plan
- Goals and priorities for the upcoming week:
  - Finishing backend implementation for **Uploaded Files and Generated Files Views** milestone.
  - Finishing unit tests for **Uploaded Files and Generated Views** milestone.
- Anticipated challenges:
  - Automating the verification of content of the files in the file views.
  - *Generated Files Views* may have issues when we actually implement the generative AI to create generated files.