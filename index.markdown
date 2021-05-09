---
layout: default
---

## Abstract

**Collaborative Sequencing (CoSeq)** is the process by which a group collaboratively constructs a sequence. CoSeq is ubiquitous, occurring across diverse situations like trip planning, course scheduling, or book writing.Building a consensus on a sequence is desirable to groups, however, accomplishing this requires groups to dedicate significant effort to comprehensively discuss preferences and resolve conflicts. Furthermore, as numerous decisions must be assessed to construct a sequence, this challenge can be exacerbated in CoSeq. However, little research has aimed to effectively support consensus building in CoSeq. As a first step to systematically understand and support consensus building in CoSeq, we conducted a formative study to gain insights into how visual awareness may facilitate the holistic recognition of preferences and the resolution of conflicts within a group. From the study, we identified design requirements to support consensus building and designed a novel visual awareness technique for CoSeq. We instantiated this design in a collaborative travel itinerary planning system, **_Twine_**, and conducted a summative study to evaluate its effects. We found that visual awareness could decrease the effort of communicating preferences by 21%, and participants’ comments suggest that it also encouraged group members to behave more cooperatively when building a consensus.We discuss future research directions to further explore the needs and challenges in this unique context and advance the development of support for CoSeq tasks.

------

## System

**Twine** is a web-based travel planning system through which group members build consensus on a shared itinerary. By scaffolding the process into individual and collaborative stages, Twine aims to support a more efficient and effective consensus building process.

In **Twine**, each member of the group is first sent to an individual screen on which they construct their individually preferred itinerary by adding and ordering items into a sequence.

![The individual screen in Twine](/assets/img/individual.jpeg)

After each member has submitted their sequence of preference, they all proceed to a shared collaborative screen.

![The collaborative screen in Twine](/assets/img/collaborative.png)

In this screen, group members can compare each other's preferred sequences, discuss, and gradually modify their individual sequences to be in agreement.

## Visual Awareness Technique

To facilitate the comparison of individual sequences, **Twine** also provides a novel visual awareness technique to facilitate the identification of agreements and disagreements in preferences.

### (1) Color-coding of Shared Nodes

{: .text-left}
To the right of each item in the user's itinerary, the system shows colored stubs that represent which other users in the group have also selected that same item. In the example, <span style="color:#d37f14;font-weight:bold">Pittock Mansion</span> was also selected by the two other members but <span style="color:#d37f14; font-weight:bold">Pastini</span> was only selected by the <span style="color:#86b95b">green group member</span>.

{: .img-right}
![Color-coding on Shared Nodes](/assets/img/color_coding.png)

### (2) Ordering Details on Hover

{: .text-left}
By hovering over an item in their itinerary, the user can see how their group members' itineraries differ in terms of the ordering of the items. Specifically, the user can see which other items their group members placed before and after the hovered-on item. In the example, the user hovers on <span style="color:#d37f14;font-weight:bold">Forest Park</span> and can see that <span style="color:#86b95b">"Frog"</span>, their group member, had the item represented by the pentagon before Forest Park.

{: .img-right}
![Ordering Details on Hover](/assets/img/ordering_details.png)


### (3) List of Missing Nodes

{: .text-left}
The _List of Missing Nodes_ helps the user see which items they didn't add to their itinerary, but their group members did. For example, <span style="color:#d37f14;font-weight:bold">Q Restaurant & Bar</span> has both the <span style="color:#86b95b">green</span> and <span style="color:#474747">black</span> stubs filled which shows that both group members have that restaurant in their itineraries.

{: .img-right}
![List of Missing Nodes](/assets/img/list_of_missing.png)

------

## Results

We conducted a within-subjects study in which 15 teams of three friends (N=45) reached a consensus on travel itineraries twice---once with **Twine** (VA) and once with a baseline that did not include the visual awareness technique (Control).

Our findings revealed that the visual awareness technique significantly increased perceived efficiency and effectiveness of the consensus building process. Also, by coding all the message from the study, we found that group members expressed their own opinions and asked about each others' less with the visual awareness technique.

{: .results-img}
![Summary of main results.](/assets/img/results_gini.png)

Participants mentioned how **Twine** helped them externalize their cognition so they could more easily remember each other's preferences and asked about these less. We also saw from participants' responses that the visual awareness technique encouraged group members to adjust their own preferences to match their group members'.

{: .center .quote}
G2P2: *"There was no need to remember in my head which [location] we all wanted to go to and which [location] only I wanted to go to."*

{: .center .quote}
G13P3: *"Having a separate list for locations that I didn’t select but my members did allowed me to conveniently adjust my opinions to match my members’ opinions."*

------

## CSCW 2021 Paper (Camera-ready)

[Link to the PDF][1]

[ACM DL Link][2]

## Bibtex
<pre>
@article{10.1145/3449250,
  author = {Kim, Tae Soo and Goyal, Nitesh and Kim, Jeongyeon and Kim, Juho and Hong, Sungsoo Ray},
  title = {Supporting Collaborative Sequencing of Small Groups through Visual Awareness},
  year = {2021},
  issue_date = {April 2021},
  publisher = {Association for Computing Machinery},
  address = {New York, NY, USA},
  volume = {5},
  number = {CSCW1},
  url = {https://doi.org/10.1145/3449250},
  doi = {10.1145/3449250},
  month = apr,
  articleno = {176},
  numpages = {29},
  keywords = {small group, consensus, collaborative sequencing, visual awareness, group communication, group awareness}
}
</pre>

------

[![Logo of KIXLAB](/assets/img/kixlab_logo.png)](https://kixlab.org)
[![Logo of KAIST](/assets/img/kaist_logo.png)](https://kaist.ac.kr)
[![Logo of Jigsaw](/assets/img/jigsaw_logo.png)](https://jigsaw.google.com)
[![Logo of George Mason University](/assets/img/gmu_logo.svg)](https://www2.gmu.edu)
{: .logos}

{: .center .acknowledgement}
This research was supported by the [KAIST](https://kaist.ac.kr) UP Program.


[1]:https://kixlab.github.io/website-files/2021/cscw2021-CoSeq-paper.pdf
[2]:https://dl.acm.org/doi/10.1145/3449250
