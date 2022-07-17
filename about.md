---
title: About the Project
description: >-
  It started out with a miss, how did it end up like this?
---

In the Fall of 2021, I was looking at the barren, landlord-beige walls of my DC-area apartment and thought about how it would be nice to have some more art for my walls.
I then thought about how other cities have blinky PCB metro maps, and given DC's burgeoning maker / tech crowd and transit / urbanist enthusiasts, someone *surely* had made one.
As it turns out, no one had.

So I decided to learn how to make one. I figured it would be a good learning exercise to learn about making custom PCB and developing embedded / IoT software (beyond very simple RaspberryPi projects).

Over the next few months, I got an ESP8266 chip talking with WMATA's API using Arduino code, poked at developing a continuous-integration pipeline for embedded software, appreciated the value
of going with what an API provides to meet my needs instead of trying to come up with a clever solution to save a few bytes, learned how to use InkScape to design artwork and how to turn that artwork
into a PCB footprint, and designed my own custom PCB that worked on the first go around!

While I'm selling the boards for more than the raw material costs (not to mention shipping costs, transaction fees, ...), I'm not making a huge mark-up or coming close to making what I would per-hour at my job.
I started this project to have some art that I could enjoy, and I want these boards to be accessible. I also don't plan on pocketing most of the profits. Aside from the occasional treat, the proceeds
will be going to local DC community members and organizations, mostly mutual aid efforts like [DC Abortion Fund](https://dcabortionfund.org/) and the [coalition of mutual aid networks supporting migrants bussed to DC](https://dcist.com/story/22/05/24/local-mutual-aid-effort-migrants-bused-to-dc/).

I have a full-time job that is not selling these boards, so don't expect the most responsive or highest-quality customer service. I want to make something that everyone can use and enjoy, but I don't have the
capacity to make this as professional and seamless as possible. 

I plan on (eventually) writing blog posts going through the entire development process, my lessons learned, etc. - especially for
the project management practices I tried to bake-in to the process (e.g. setting up a CI pipeline, creating an auto-updating bill-of-materials). 
Until then, the source code is public; feel free to reverse-engineer my mistakes from the commit history.

<img class="headshot-img" src="{{ site.baseurl }}/images/headshot.jpg" alt="Picture of me, Logan, a young, white male with a short beard wearing purple sunglasses and black guayabera. I'm standing in front of a wall at Metrobar with art on it, to the right is a pink astronaut with a patch that says '51'">

## About Me

I am a part-time open-source software developer (would say hobbyist, but you're paying for these boards), transit enthusiast (#NUMTOT-confirmed), hacker, and community member. If you really want to know more, I have a personal website at [loganarkema.com](https://loganarkema.com).


<style>
  .headshot-img {
    float: right;
    margin: 5px;
    width: 25%;
    height: auto;
  }
</style>