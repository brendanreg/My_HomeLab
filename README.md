# My_HomeLab
Started 11/15/2023

I decided to start small with my lab. Being limited in space and having roommates has its constraints. Additionally, at the time of writing I still consider myself to be a beginner in the realm of information technology, and acquainting myself with highly affordable technologies seems like a nice enough idea to me. With that being said, the first step is acquiring the necessary hardware for my project. So let's begin.

## Initial Parts List
The following is a parts list for my lab **at the time of writing 11/16/2023**
### * Raspberry Pi 4B (8GB)
### * Stackable Raspberry Pi Case with fan/heatsink
### * 128 MicroSD card
### * Power adapter
### * Micro HDMI to HDMI cable

I wanted to get up and running quickly so I elected to use plain old Raspbian as my operating system.

## First Order Of Business
My plan from the beginning was to use the rpi4 as a tiny server for menial tasks such as a plex server for home entertainment, so I started there. Should be easy enough. just download the necessary packages, apt-get yada yada yada, restart the pi and open the html Plex interface. Everything looked great until I realized while tinkering with my streaming settings that I was on limited bandwidth (of merely 1mb/s!) due to a double NAT problem... that's interesting because there shouldn't have been a double NAT problem to my knowledge. The internet for my rpi was coming from a powerline adapter hooked up to the router downstairs but upon closer examination I realized the rpi was running on a network with an SSID completely different from the rest of my devices. I did some looking around and realized the house had a 2-in-1 modem/router, which was newer and supplyinmg internet to most of the house, while the powerline adpater providing internet to my rpi was actually connected to a seperate netgear router which was in-turn connected to the aforementioned modem. That's why there's a doubel NAT problem. Unfortunately, due to some constraints I don't have the time to get into, switching the adapter to the modem wasn't going to happen, so I had to use some clever thinking to figure out a workaround... luckily I had just learned about port forwarding whgile studying for the CCNA, and decided to do a bit of research and after a half hour of tinkering with the port forwarding settings on both my modem and my router, the problem was fixed. Woo! first hurdle clear without a single scratch on me.

## Updates
Since my initial setup of the rpi and plex server, I've added a 4tb hard drive to my lab to act as storage for my plex and other miscellaneous stuff, essentially turning my rpi into an underwhelming NAS. I also picked up the most affordable netgear managed switch I could find so I could more efficiently manage my ethernet connections and get a foothold on cable management.
