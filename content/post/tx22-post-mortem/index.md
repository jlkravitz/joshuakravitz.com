---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "What happened in TX-22?"
subtitle: "Democrats hoped to flip TX-22, but ended up with worse margins than in 2018."
summary: ""
authors: []
tags: []
categories: []
date: 2020-12-06T10:39:44-08:00
lastmod: 2020-12-06T10:39:44-08:00
featured: false
draft: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

From June through November, I was the Data Director for the TX-22 Congressional Race, where Democrat Sri Preston Kulkarni was hoping to flip the district's congressional seat to the Democratic Party. A member of the Red-To-Blue DCCC funding program, this was one of the most closely watched congressional races in the country. Going into Election Day, we felt good about our odds, but our optimism faded as the election-night returns started flowing in at 7:15pm CST: we were losing by larger-than-expected margins.

Ultimately, we lost by 6.9% – a disappointing outcome, given Kulkarni's 4.9% margin loss in 2018.

Curious, I dove into the data and attempted to answer the following:

* What happened?

* What could we have done differently?
* What does TX-22 say about other races up and down the ballot in TX and the entire country?

Before diving into the analyses, I'll start with some history and context on TX-22.

## An Overview of TX-22



| Year | Race      | Votes  | Turnout | Dem Margin |
| ---- | --------- | ------ | ------- | ---------- |
| 2016 | House     | 305543 | 70.5%   | -19%       |
| 2016 | President | 308653 | 71.2%   | -7.84%     |
| 2018 | House     | 297405 | 60.7%   | -4.9%      |
| 2018 | Senate    | 299335 | 61.1%   | -0.64%     |
| 2020 | House     | 408048 | 73.1%   | -6.9%      |
| 2020 | Senate    | 411224 | 73.7%   | -6.2%      |
| 2020 | President | 420932 | 75.4%   | -0.98%     |

| Year | Registered Voters |
| ---- | ----------------- |
| 2016 | 433510            |
| 2018 | 490118            |
| 2020 | 558118            |



How did we fare compared to other races in TX-22? How did the Democratic margin compare across races in TX-22?

* * President
  * Senate
  * County Judge & Fort Bend Sheriff (ask Sri which ones we care about)
* What did the raw undervote look like down the ballot?
  * President to Senate, Senate to Congressional, Congressional to Sheriff, etc.
* How did our undervote compare to other congressional districts?
  * e.g., Is the President Dem Margin - Congressional Dem Margin generally smaller, larger, or the same compared to other congressional districts? (Can run a t-test here.)
  * It's possible this difference is greater in our district: if it is, I'd be interested in seeing how we compare to more down-ballot races. Is the difference larger here, too? That would imply we consistently underperformed ... why? Is the difference smaller? Maybe we're more well-liked than the down-ballot races? Maybe there was a lot of ballot drop-off below the congressional level? Maybe something else?
* How did ballot drop-off fare across constituencies? Who wasn't voting down-ballot?
* How did different constituencies vote?
* Did Nehls' name recognition have an effect on the outcome?
* Effectiveness of programs
  * Who answered the phones? Who refused? Who *didn't* answer?
  * Who came out to vote that we called? Who didn't? Matching study –– effect of a call.
  * Same thing effect of a text.
  * Relational –– effect of a contact (how good is this data though).

## By Constituency

