---
layout: post
title: "Life Update"
subtitle: "Some current status update"
---

Today I want to to give a brief status update of my life because, since my last
post, some major changes have occured.

Last semester of my studies was a huge progress towards achieving my bachelor
degree. It was the most productive semester ever. I achieved 32,5 ects while
working part time which is personally a accomplishment for me. I made the mistake
that I never made the risk to assign to more classes because I didn't want to
fail the class. But retroperspectively this wasn't a clever decision. I would
have reached my goal faster, if I would have taken more classes eventhough of
failing some classes.

Also I moved to another job. In april I will work for
<a href="https://www.s-itsolutions.at/">s IT Spardat GmbH</a> which belongs to
the Erste Group. I am also looking forward to this new challenge. My aim is to
learn as much as possible and broaden my horizon. Also I want to contribute as
much as I can and try to settle down as fast as possible.

While I was applying for jobs, I also made a side project which is called
<a href="https://github.com/janmichaellaranjo/CourseAnalyzer">Course Analyzer<a/>
to acquire some web front end skills. I made an application which gives a clear
overview of the progress of your studies because the process of counting all
ects and comparing courses is so tedious. The application needs a file that
contains the finished courses, the study plan and a transitional provision file
which is optional. The result of the analysis is the list of remaining courses
and unnassigned courses and the sum of the achieved ects for mandatory courses,
optional modules and transferable skills.
At first I created a <a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/web.html">Spring MVC application</a>
which already included the front end. For the front end I used
<a href="https://angularjs.org/">AngularJS</a> at first (I know that this was a
bad decision but I also wanted to learn the process of migrating). I easily set
up the front and back end. I designed the architecture in way such that the
implementations for analyzing files can be easily replaced because the
extraction of content heavily depends on the expected format and content of the
files. I implemented the analysis for formats of the study plan, transitional
provision and course list which includes all finished files for the TU Wien's
curriculum in <a href="http://www.informatik.tuwien.ac.at/">computer science</a>.
I also made some unit tests to maintain a certain software quality.

Unfortunately AngularJS's concepts are bit confusing and maintaining or
correcting became a bit tedious. So I moved to Angular. At first it was a bit
confusing to migrate from AngularJS to Angular and I decided to redesign the
whole front end. In the end the result was much more responsive and the design
of the front end in general was much cleaner than in AngularJS.

This semester I also started with my bachelor thesis. During my discussion with
my supervisor we concluded that I should a serious game that focuses on voice
disorders and voice hygiene. I am also keen finally start writing and
programming the application, after I made the necessary planning and
consultations of experts. When everything goes well, I will finish this bachelor
studies this semester or at least the beginning of the next winter term.

I hope this post gave you a clear overview what happened the last months and my
future plans for this semester and my work life. There will be more updates,
when some major events happen.
