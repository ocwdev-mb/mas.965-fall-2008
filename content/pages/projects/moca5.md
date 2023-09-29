---
content_type: page
description: ''
learning_resource_types:
- Projects
ocw_type: CourseSection
parent_title: Projects
parent_type: CourseSection
parent_uid: 7b53ea3b-401e-0767-1816-c31fc0eee770
title: Compiled Status Entries
uid: fcf14489-aefb-e76a-3cc5-4180ba2cef6a
---

**Mobile Diagnostics**  
**Project News Archive**

**Mobile diagnostics in the developing world**  
September 20th, 2008  
Re-posted from [Ted Chan's blog](http://gettogreen.blogspot.com/2008/09/open-innovation-for-health-care-in.html)

What do you get when you squish a project with General Electric to transmit ultrasound images in Belize and a project with Center for Infectious Disease in Zambia (CIDRZ) to diagnose cervical cancer in rural areas? I'm finding out over the next three months by using my technical project management skills on an important project to figure out how to transmit images over low bandwidth mobile networks.

The goal is to build a scalable technology to transmit, annotate and manage these records. The key bottleneck in health care in the developing world is human resources. You need an approach for telehealth where image capture can be done by a layman in a rural area. The image can be transmitted and then worked on in a different location (anywhere in the world) where medical expertise is more readily available.

This is necessary for successful preventive screening models in rural areas where clinics might be far from the patients who cannot spend much time away from home. In cervical cancer, one of the biggest problem is loss of patient to follow-up. Near real-time diagnosis using a vinegar swab prevents that as the patient never leaves the clinic while waiting for their diagnosis.

Figuring out some of the key requirements will definitely be a challenge. We've heard 100KB or 3MB. That's a big difference in terms of what type of technology, transmission times, compression, etc. that you would use. We discussed how the key bottleneck in health care in the developing world is human resources. You need an approach for telehealth where image capture can be done by a layman in a rural area. In this case being piloted in Belize exams will be carried out by non-expert sonographers who can send by mobile link to radiologist. DICOM communications server will be used with a database for archiving images and a image reviewer. Currently, GE data system aggregates a series of data, but the process is a bit complicated for a rural health worker. We'll need to look at this process closely in our needs assessment. The idea is to come up with something that can be scaled and re-used across many developing nations.

Currently, GE has a pilot project going on in Belize. 270 scans were taken in Belize by rural health workers and transmitted using a prototype device. They are conducting full statistical study with panel of five radiologists will score images on whether the quality is sufficient to make diagnoses.

GE's ultrasound system will address several areas, including pregnant mothers, but also functions like sweeping for typical issues of the thyroid, kidney and gall bladder.

I'm looking forward to learning more about the Zambia process as well - this project is underway as a prototype was developed earlier this year, but the architecture we develop will be important in making it a sustainable model. Here's an overview of the project.

{{< resource b8d3cb2e-224f-7f1c-ce8e-28d0a81f0777 >}}

I'm going to be posting out updates throughout the next three months that we'll be working on this project. Your feedback would be great. This really is the best type of open innovation project. We have leading faculty from MIT, Harvard, one of the top companies in the world in GE and an important non-profit in CIDRZ. The core project team is two bioengineers, an industrial designer from the Media Lab, a programmer and me, the MBA. Let's see how it goes and if we can help make a big leap scalable across the developing world in improving rural health care.

{{% resource_link "f456e17f-d352-fd77-73a1-7a0ae12d14c4" "« back to MoCa" %}}

**Solution evolves towards medical image workflow management**  
September 21st, 2008  
From [Ted Chan's blog](http://gettogreen.blogspot.com/2008/09/open-innovation-for-health-care-in.html)

Some updates on the MIT NextLab/global health project that I'm working on. Originally, CIDRZ and GE were supposed to be stakeholders, but due to bandwidth concerns, we're primarily focused on the CIDRZ project and improving the workflow to diagnose and treat cervical cancer. However, having GE involved made us think about some of the more general issues that are out there, and we're trying to build a solution that is scalable and solves a few of these.

One is that there doesn't seem to be a good system out there that can manage image/video based workflow and take multiple inputs. As such, we're moving towards a system that integrates workflow and the tagging, commenting and return diagnosis features. Think a Flickr like site integrated with records management that can accept incoming images a number of ways including e-mail, via mobile phone, web or USB upload. We'll try to build it so it can integrate relatively easy with existing medical record systems. Comparing it to Flickr is a bit of an oversimplification, since the application should allow for a lot of features, such as creating a queue for radiology experts in different locations to review, return a diagnosis, store medical records for future reference, etc.

We're also exploring the possibly of using Eye-Fi or other technologies to accelerate the transfer speed and more importantly, streamline the steps necessary to transfer the data. One of the problems with existing smartphones is that they ask permission to run applications and send data. So applications that sling data back in forth in an automated manner help the process flow a lot.

We're realizing that this has the potential to scale out not just the CIDRZ model, but be re-usable for other rural health models. It's interesting to think about this in terms of being able to help millions of people. The Emerson communications team that is working with us to document the project will be posting some videos soon for anyone who is interested in learning more about the project. Any ideas or possibilities for collaboration are welcome!

{{% resource_link "f456e17f-d352-fd77-73a1-7a0ae12d14c4" "« back to MoCa" %}}

**NextLab team collaborates with OpenMRS to scale solution**  
October 1, 2008  
From [Ted Chan's blog](http://gettogreen.blogspot.com/2008/09/open-innovation-for-health-care-in.html)

I learned in my stint as an enterprise IT strategy consultant that IT is like the holy grail in Indiana Jones and the Last Crusade. Just as good technologies gives life, bad technology takes it away. Never has that statement been so literal as it is in developing world health care.

As I mentioned in previous post, our project with CIDRZ to improve cervical cancer diagnosis in Zambia has evolved towards the workflow management back end to allow physicians to remotely review, diagnose and provide feedback on images. An exciting development is that we'll be working to make this fit in with the [OpenMRS](http://www.openmrs.org/) system. OpenMRS is an open-source medical records system that is gaining traction in the developing world. If the goal is scalability, and having an impact beyond Zambia into the entire realm of developing world medical imaging, compatibility with OpenMRS is an extremely important step.  This will allow for what we develop to be leveraged and re-used and evolved.

At the Open Innovation Workshop that I attended in May, many of the younger PhD and me were wondering about models where collaboration and innovation enable by new ICTs could save this world. OpenMRS is an example, albeit one fraught with potential pitfalls. Medical records are an issue and a major cost for health care providers everywhere in the world. By providing a scalable, open source system and getting talented developers to work on add-in modules, OpenMRS offers a solution for providers looking to keep information technology costs low. This enables the providers to spend the money on what really matters – treating patients.

I'm curious to learn more about OpenMRS – it looks scalable and robust from its data design. It's been deployed in a number of developing world locations. If it works, it will allow providers to divert money towards where it really matters.

There's another team working on a front-end Android interface for medical records imaging led by Zach Anderson, a MIT Course 6 programmer that we are collaborating with as well. It sounds like they too will be compatible with OpenMRS. More on that collaboration in another post as I learn more about what specifically they are doing.

{{% resource_link "f456e17f-d352-fd77-73a1-7a0ae12d14c4" "« back to MoCa" %}}

**Debating GPL versus BSD software license**  
October 27, 2008  
From [Ted Chan's blog](http://gettogreen.blogspot.com/2008/09/open-innovation-for-health-care-in.html)

Trying to figure out whether to use the GPL or BSD license. Numerodix had a good simplified explanation on it:

*   _In the GPL license you have the four freedoms: to run the software, to have the source code, to distribute the software, to distribute your modifications to the software. What this implies is that when you obtain the software, you have the \*obligation\* to ensure that these four things hold true for the next person you give it to. After all, someone had to go to the trouble of preserving these rights for \*you\*, so you have to do the same for the next guy._
*   _The BSD license is different, because it gives \*you\* the right to distribute the software, but it does not oblige you to make sure that the next guy has any such right. Well, that's not really a problem, the next guy can ignore you and get the software from the same source that you did (if that source is still available). But if you change it and you give it to him, you can forbid him from passing it on._

See the [Numerodix blog post](http://www.matusiak.eu/numerodix/blog/index.php/2007/12/15/gpl-vs-bsd-a-matter-of-sustainability/) for a more detailed explanation.

FossWire also has a [good comparison here](https://fosswire.com/post/2007/04/the-differences-between-the-gpl-lgpl-and-the-bsd/).

What are we going to do with our open source mobile diagnostics workflow solution? As an open source software project, we'd like to license it out for non-profit use and use in the developing world for free. But we also think it's possible our software might be modified for for-profit use in the developed world. In this case, we would want a reciprocal contribution - a donation, either in funding or code. I'm thinking that means GPL. GPL means that if another organizations uses or modifies any code your organization produces that code must also be licensed under the same terms.

{{% resource_link "f456e17f-d352-fd77-73a1-7a0ae12d14c4" "« back to MoCa" %}}

**Update on application progress**  
November 10, 2008

_Application Development_  
This is what the system can currently do:

1.  Load a doctor-defined form and run it. We call these forms "procedures." Procedures can prompt using various entry techniques (check boxes, radio buttons, text entry, etc.) and they can acquire various types of data (currently pictures and sound)
2.  If pictures are acquired, multiple pictures can be taken and reviewed. In the review dialog, health workers can zoom in and pan across the photo. They can then select which photo(s) they want to send back.
3.  The procedures fully support branching. This means that questions can be set up to be displayed depending on the answers to previous questions. For example, if a question asks "where is the pain?" and the person answers "chest" then a series of specific chest pain questions can follow.
4.  The health worker can see the current progress of the procedure at all times via a progress bar in the title.
5.  The acquired data is sent back in a packetized format. We are still working on packetization and off-line synchronization, but we are currently able to do some rudimentary upload packetization.
6.  The filled-out form along with pictures, sounds, etc. is sent to the MoCa Dispatch Server, a program that communicates with the mobile phone app, does the data packetization/integrity checking, and sends the data to OpenMRS. The MoCa Dispatch Server currently uses an OpenMRS "plugin" we wrote. This means that we can write other plugins for the dispatch server so that, in the future, we can support other records systems if we please.
7.  OpenMRS receives the picture and question/answer pairs. This information is tagged to a patient and can be accessed via the "medical images" tab in OpenMRS.
8.  A queue running on OpenMRS lines up all pending diagnoses awaiting physician review. Clicking on one of the records brings up the question/answers and the image. The image is pan/zoom-able.
9.  The physician can annotate the image with his/her diagnosis. Upon making this annotation, it will be immediately sent to the phone that acquired the data. The physician can see the phone number of the phone that sent the data, so he/she can call the health worker too.
10.  As soon as this annotation is made and sent to the phone (via SMS because it is cheaper and more reliable than GPRS) the phone gets a pop-up saying that a diagnosis has been received for the particular patient number. The health worker has the option of bringing up a window to see the full annotation sent back from the physician, or he/she can dismiss the pop-up and look at it later.

As you can see, we have a complete end-to-end solution in place. While there is still a good deal of work ahead, we now have something that works. I'll send out screenshots once I get a chance to grab some.

_Website_  
I registered a SourceForge Open Source project and it was approved today. They will host the code and allow others to contribute to the project. I have also set up a Documentation Wiki; there currently isn't anything on the Wiki, so in the coming few weeks we will want to start documenting the system.

{{% resource_link "f456e17f-d352-fd77-73a1-7a0ae12d14c4" "« back to MoCa" %}}

**Update on new partners**  
December 1st, 2008

Leo Anthony Celi, our MD advisor from Harvard Medical School, recruited new partners in ASEAN Centers for E-Health and Telemedicine as well as the following universities:

*   Universiti Sains Malaysia (Malaysia)
*   Institut dela Francophonie pour Medicine Tropicale (Laos)
*   University of the Philippines Manila (Philippines)
*   University of Gadjah Mada (Indonesia)
*   Ciputra Univerity (Indonesia)
*   Hanoi Medical University (Vietnam)

We're looking at deploying in the Phillipines in January through March and learning more about how MoCa can meet the needs of patients there.  Things are breaking fast for MoCa - there seems to be a ton of interest in our solution.

{{% resource_link "f456e17f-d352-fd77-73a1-7a0ae12d14c4" "« back to MoCa" %}}