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
uid: 3fa7c88e-dee3-e4eb-ffaa-7af6ca47f933
---

**Disaster Management / NextMap**  
**Project News Archive**

**Prototype Interface**  
October 17th, 2008

We're just receiving messages in two formats, "locate" and "message", and mapping them. Users can currently SMS in "locate 30 Ames St, 02139", for example, and their number will be assigned to that location. They can then send "message theres a firetruck here" and the words "theres a firetruck here" will appear at 30 Ames st on the map.

Next we're looking to solve outgoing message problems and to allow users to enter relative movements, i.e. "move 500 meters north". We're also thinking of adding placemarks, like "mark as office", so users can later send "locate office" and will be updated to that personal placemark.

Geocoding of the textual address is done via GeoKit ([https://github.com/glebm/geokit-gem](https://github.com/glebm/geokit-gem)), a Ruby on Rails geocoding plugin. The prototype itself is made in Ruby on Rails and uses the Google Maps API.

{{% resource_link "4a2d649b-f7aa-7691-6f23-275d621a0437" "« back to NextMap Disaster Management" %}}

**Interface Snapshot**  
October 21, 2008

{{< resource "f17c7f70-7ff9-c543-546d-f5a5dde35a9c" >}} 

  
Thinking about interfaces for viewing data in an interactive map - beyond Google Maps. This is done in Quartz Composer as a prototype - it draws on live map data from our server prototype.

See [video of this interface in action](http://www.flickr.com/photos/jeffreywarren/2963528378/) \[Flickr, 0:21\]

{{% resource_link "4a2d649b-f7aa-7691-6f23-275d621a0437" "« back to NextMap Disaster Management" %}}

**InnovGreen: Q&A**  
October 22nd, 2008

Young Yang, our contact from Flow, Inc. in Taiwan, has been a big help in translating our communication with Vietnam from English to Chinese, which is the language of choice for Forestry Department manager, Mr. Chu.

Our last two conversations have uncovered a crucial piece of information: that the forest inspectors will be the ones operating the mobile phones in remote, deforested regions of Vietnam, not the famers. Here are some key Q&A's:

_Background questions_

*   Where are the regions in Vietnam this system will be used?
    *   Kontum
    *   Lang son
    *   Nghe An
    *   Quang Nam
    *   Quang Ninh

*   What is cell phone connectivity like in those areas?
    *   Poor in forestation areas
    *   Normal cell phone coverage in district down town
    *   Acceptable in province central town. In Ha long and Kontum there is GPRS service

_User-interface design questions_

*   What is the literacy rate of farmers in Vietnam
    *   93% overall country, but in remote where IG plan to have land, the rate is about 8x% only

*   Will the farmers have to upload the data to a computer or will someone else do this for them?
    *   InnovGreen forest staff will do tha

*   How often do farmers use the internet, if at all?
    *   rarely at commune post office

*   Any other UI requirements please specify here:
    *   Vietnamese and Chinese UI as a customisation.

_Operational sustainability_:

*   From where do you recruit the farmers?
    *   from plantation surrounding communes either directly or indirectly through contractors

*   Who is the contact person communicating with the farmers? Where does this person reside?
    *   IG forestry staffs, they stay in temporary offices nearby to the plantation area

*   What is the current process for farmers to show that they have fertilized an assigned location?
    *   Contractors distribute the fertilizer to farmers-workers at morning and take back the empty package by the end of working day

_Project Timeline_  
 

> 10/22: Initial System Design  
> 11/01: Financial & Operational Sustainability Analysis  
> 11/19: Mid-project report  
> 12/03: Working demo  
> 12/10: Final presentation

{{% resource_link "4a2d649b-f7aa-7691-6f23-275d621a0437" "« back to NextMap Disaster Management" %}}

**Design Tradeoffs**  
November 17th, 2008

As our project time enters its last month, we have started taking the abstract ideas from our design sessions and information generated from speaking with our partner organizations to begin an actual implementation that we will be presenting at the end of the semester.

My current work on our software implementation is the development of a client-side J2ME application to be run on cell phones for Catholic Relief Services (CRS).  The primary purpose of the application is to allow CRS field agents to populate a 50-question survey that provides basic information about a disaster when it hits a given region and then send that information instantaneously to a server, which will log it and allow CRS to allocate resources accordingly.

NextLab had previously worked with CRS last semester (when it was called ICT4D), and a group had written a J2ME application already that handled some of our task.  This is where some of the basic design trade offs in our application would come into play.

The application developed last semester does a really nice job of allowing flexibility in the forms that can be used in the application (forms are written in XML, opened by the application, and then answers are parsed into a string that is sent via SMS to a server, which populates a database entry based on the received SMS). 

One problem with this design is that for the survey we are using, which has 50 questions (some of which have many parts and data fields), there is almost no way that all the answers will fit in the space of a 160-character SMS message.  This poses a financial sustainability problem, since we will require many SMS messages to send a single survey's answers.

A possible solution to this (which I am implementing this week) is using compression at the binary level (i.e. for a yes/no question, I only need 1 bit to represent the answer, for selecting 1 of 8 = 2^3 choices I need 3 bits, etc.).  While this will almost surely allow us to compress the 50 answers into 1 SMS message, significantly saving costs.

However, the tradeoff here is that both client and server side will need to create compression that is specific to the form, which will require significant editing of the source on both the client and server side, which is not optimal from an operational sustainability perspective.

Over this week we will be making a lot of decisions regarding this trade-off, and one of the big questions will be discovering what matters more, costs of SMS or the flexibility to change the form?  If the form has been the same and will be for the next 10 years, then hard-coding compression will make much more sense.  If it changes every month, then we need a more flexible model. 

In the end, I would like to implement some hybrid compression model that perhaps uses some metadata in the XML form that customizes compression.  For the moment though, the priority will be to create a functional system that solves CRS's problems and is as efficient as possible depending on their priorities.

More info on solving these problems to come soon!

{{% resource_link "4a2d649b-f7aa-7691-6f23-275d621a0437" "« back to NextMap Disaster Management" %}}

**Nextlab Disaster Management teams up with OpenROSA**  
December 25th, 2008

I'm proud to announce that we are days away from the release of a totally revamped version of our J2ME application that is being used for Disaster Management with Catholic Relief Services in India.  We have been working closely with the OpenRosa consortium (specifically on their JavaRosa code base, which is an open source platform for developing data collection applications on J2ME enabled cell phones). 

For any of you who are developing applications for mobile data collection, I highly recommend getting in touch with these folks.  They do a beautiful job of abstracting out the different parts of collecting and transmitting data, and I was very easily able to create customized UI functions, data parsing, and SMS protocols.

On the subject of our earlier post regarding design tradeoffs and data compression for this application, we decided to go with sending multiple SMS messages (with our system we get about 6-8 SMS messages for a fully filled-out form.  We chose to do this because we wanted to allow the user to not be limited with regards to how many digits they could type for answers or how long they could make string values.  Instead, we made an efficient XHTML form and used customized message parsing and SMS splitting in JavaRosa to reliably transmit bigger message payloads to Twitter and then subsequently to a server.

Happy holidays to everyone, and lets keep giving the gift of technology to those who need it most!

For more information on OpenRosa and the JavaRosa code base, please check out:  
[http://www.openrosa.org](https://bitbucket.org/javarosa/javarosa/wiki/OpenRosaAPI)

{{% resource_link "4a2d649b-f7aa-7691-6f23-275d621a0437" "« back to NextMap Disaster Management" %}}