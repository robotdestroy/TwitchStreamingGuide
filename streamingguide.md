![](https://cdn-images-1.medium.com/max/1250/1*mZ5h_tgeAB_jFC2eOKnvng.png)

#### The Chill and Sorta Comprehensive

# Beginner’s Guide to Streaming on Twitch

Lately I’ve been fascinated with watching people stream on
[Twitch](https://www.twitch.tv/). I like the deep cut channels the most, people
who have 0–5 viewers. I feel like I get to peak into their lives, watch them
play games, make things and generally be awkward and bizarre.

For whatever reason I too feel compelled to participate in this medium and I’ve
spend the past few months learning and exploring how it all works. I thought I’d
share what I learned so far. One of the most rewarding parts of the experience
has been exploring and playing with the tool-set streamers use. It’s a different
kind of creativity than I’ve experienced before and it’s really fun.

### 1. Basics

#### Twitch Account

This is obvious, but you will need an account on
[Twitch](https://www.twitch.tv/) to get started. Follow and friend everyone you
know IRL. This will be helpful later on.

![](https://cdn-images-1.medium.com/max/1000/1*ehy78qjrKPDyMVImBfn_Gg.png)
<span class="figcaption_hack">This is OBS and I’m also in the process of moving</span>

#### OBS

[Open Broadcaster Software](https://obsproject.com/) is very capable software to
broadcast your stream to Twitch. I’ll walk you through the basics of what you
need to know.

1.  Download [OBS](https://obsproject.com/) and install. If you are using Windows,
right click on OBS and ‘Run as Administrator’ so it automatically grants the
software permissions to capture your games.
1.  Open Settings and select ‘Stream’. Select Twitch as the ‘Service’.
1.  Open [Twitch](https://twitch.tv/) in your browser and select ‘Dashboard’ from
your menu in the upper right corner. Select ‘Settings’ from the left nav, then
select ‘Stream Key’. Tap ‘Show Key’.
1.  Paste the key in the OBS field called ‘Stream Key’.
1.  Congrats, you can technically start streaming now!

#### Something to Stream

Maybe you want to stream games, maybe you want to stream yourself working or
maybe you just want to stream yourself on camera. You need something to stream.
Here is how you set that up:

![](https://cdn-images-1.medium.com/max/1000/1*oqWAmJOkPwVwvH3nEJrZSw.png)
<span class="figcaption_hack">Adding a game capture window source</span>

**Games**

It is likely that you are interested in streaming games. If it’s not games you
are interested in, most desktop applications can also be streamed using this
same technique:

1.  Go to the sources panel in OBS and press the + button. Choose ‘Game Capture’ and
enter the name of the game or application you want to stream in the ‘Create New’
field.
1.  Open the game or application and select ‘Capture Specific Window’. Press OK.
1.  Choose your application in the Window drop-down. Press OK.

You will want this source at the bottom of your ‘Sources’ list. The list mimics
the visual hierarchy of sources and you are going to want to overlay other
sources on top. You may need to resize the source. You can do this by dragging a
corner of the source and snapping it to the edges of the full window.

![](https://cdn-images-1.medium.com/max/1000/1*tTT1-RFlkmMlmvfyCvcE4A.png)
<span class="figcaption_hack">Move or preposition a source when selected.</span>

**Desktop**

Maybe you just want to stream your whole workspace. I usually don’t do this
because it feels pretty dangerous. I prefer to not broadcast open browser
windows and such, but if you like living on the edge you can stream everything
your computer is displaying using this technique:

1.  Choose ‘Display Capture’ as your source.
1.  Enter a name and press OK.

**Camera**

One of the main enjoyments of watching a stream is seeing someone react and
express themselves. I highly recommend streaming with a camera.

![](https://cdn-images-1.medium.com/max/1000/1*rJFD7pHA3N3KttdERQhdvA.png)
<span class="figcaption_hack">Adding a camera video capture source</span>

This may feel awkward at first but you will get over it. It’s really no
different than how you present yourself all day long. Just be yourself.

1.  Choose ‘Video Capture’ as your source. Name it ‘Camera’.
1.  Choose your camera and press OK.
1.  Place the source above the Window Capture in the sources list and resize the
source to your liking.

In most cases, you will also need to add your microphone as a ‘Audio’ source.

**OBS Stream Settings**

This section is likely to be the most contentious information I provide. OBS
stream settings can be a bit like black magic. The best settings vary widely
with people’s particular setups. Serious streamers use a second computer to
encode their streams so they don’t eat up resources from their main device.

![](https://cdn-images-1.medium.com/max/1000/1*xEDbzcuU8ylK0nLzRR5mkA.png)
<span class="figcaption_hack">My OBS stream output settings</span>

I’m going to share with you my settings, which work for me. I encourage you to
go check out the [thousands of videos on
YouTube](https://www.youtube.com/results?search_query=obs+settings+for+twitch)
about various other setups if you don’t find these to work to your liking.

1.  Open OBS and choose ‘Preferences’.
1.  Tap the ‘Output’ category.
1.  Set your ‘Video Bitrate’ to 3500.
1.  The ‘Encoder’ should be set to be ‘Software (x264)’.
1.  ‘Audio Bitrate’ will be 160.
1.  Set your ‘Output’ to 1280x720 with bicubic downscaling at 60fps.

These settings are fairly conservative but I think they are a nice balance point
of performance and quality. I prefer frame rate to resolution but in certain
situations you might prefer the opposite. Some streamers push a significantly
higher bitrate, but keeping your bitrate lower makes it easier for people to
watch your stream, especially on lower bandwidth connections.

### 2. Advanced Tools

With the basics out of the way, you can proceed in your streaming and probably
have a good time, but the rest of this article is where I think all the fun is.
Let’s add some functionality to our stream:

#### Overlays

Overlays let you place data on top of your stream. The point of an overlay is to
give your viewers more information to latch onto so they don’t get bored and
leave if the stream gets dull.

You can theoretically do anything but certain overlays are more obviously
advantageous. Think of them as similar to how news tickers or sports statistics
keep your mind active as a viewer.

![](https://cdn-images-1.medium.com/max/1000/1*V2aezuQOM1Jyv5__gOqhqQ.png)
<span class="figcaption_hack">The name of our Discord sits at the the top left of the screen.</span>

**Logo/Branding**

I believe putting some sort of unique mark on your stream helps you initially
express a bit of personality but also allows your viewers to instantaneously
recognize that you are serious enough not to be doing this by accident. To add a
static image overlay:

1.  Go to the ‘Sources’ panel, tap + and choose ‘Image’.
1.  Name the image source and press OK.
1.  Select the image from your local drive and resize.

Unless you specifically want a rectangular image, you will want to choose a PNG
image with transparency. This can be created in most image or design tools.

![](https://cdn-images-1.medium.com/max/1000/1*H-FPkNYpf-HPGavmoiBNUQ.png)
<span class="figcaption_hack">A round of PUBG with Clay Houser, Jeff Shafar, and Gabriel Valdivia.</span>

You can use this same technique for any sort of image. For example, I like to
put little stickers of the people who I am playing with next to my video so
people can have an idea of who are the voices on the stream.

**Alerts**

If someone follows you, alerts allow you to celebrate it in real time with your
viewers. You can let the person know you appreciate the attention and also let
them bask in the glory of interacting with the televisual in real time.

![](https://cdn-images-1.medium.com/max/1250/1*94-jQM7QFtYJFgAOwzGKkA.png)
<span class="figcaption_hack">I just followed myself.</span>

The best service I have found to set up alerts is
[Streamlabs](https://streamlabs.com/). This is a separate site which you can log
into with your Twitch account. Here’s how to set up your alerts:

1.  Tap ‘Widgets’ in Streamlabs left panel.
1.  Tap ‘Alert Box’.
1.  Press ‘Copy’ next to ‘Widget URL’.
1.  Open OBS and add a new source for ‘BrowserSource’. Name it ‘Alerts’ and press
OK.
1.  Paste the URL into the URL field and press OK. Position and resize the source in
the main view.

This will get your alerts working. You can test by pressing ‘Test Follow’ in the
Streamlabs Alert Box page. You should see the alert show up in the OBS view with
a sound.

The entire Alert Box interface can be fully customized from the Streamlabs
interface. You can choose fonts, colors, animation styles, etc. These
customizations can even be set up for specific type of alerts. ‘Subscriptions’
can be more special than ‘Follows’ for example.

![](https://cdn-images-1.medium.com/max/1000/1*MizF-NqfmATiIQ4gUNFADA.png)
<span class="figcaption_hack">A follower goal and some of my recent follows.</span>

You can also use Streamlabs for a variety of other overlays such as a recent
activity list, goals, chat box and viewer count. Take a peek through their
widgets and set up ones that make sense for your stream. Adding these sources of
activity to your stream can be helpful to show your viewers what you are
interested in and also a source of things to chat about.

![](https://cdn-images-1.medium.com/max/1000/1*y4dK6xDFzubsG54msnvEJQ.png)
<span class="figcaption_hack">Snip allows you to show what you are listening to on your stream.</span>

#### Snip

If you like to listen to music while you are streaming check out
[Snip](https://github.com/dlrudie/Snip/) (Windows only). Snip runs in the
background and can create text and image overlays of the current song and
artwork from many music services and apps such as Spotify and iTunes.

1.  Download [Snip](https://github.com/dlrudie/Snip/releases/latest). Expand the
package and launch the application named ‘Snip’.
1.  In your taskbar, right-click on Snip. You can select your service here.
1.  Play some music and Snip should generate a file in it’s directory called
*snip.txt* as well as an image file named *Snip_Artwork.jpg*.
1.  In OBS create a new ‘Text’ source. Let it read from a file and select the
*snip.txt* file in the Snip folder. You can format how the text is displayed in
OBS.
1.  If you would like a thumbnail as well, you can create a new ‘Image’ source and
select the *Snip_Artwork.jpg* file.

There are also other cool options to Snip, such as breaking out the metadata
into separate files which allows to set up layouts like the one I use. You can
do this by selecting ‘Create Separate Files’. Snip also supports useful hot keys
in the settings.

#### Scenes

You may have noticed you can quickly get overwhelmed with all the possibilities
of these sources. That is what ‘Scenes’ are for. In OBS you can set up multiple
scenes that you can switch to on the fly during your streams. I have 4 main
scenes I use:

![](https://cdn-images-1.medium.com/max/1000/1*uD0L4V_V9wAPZ0Br3qh6ZQ.png)
<span class="figcaption_hack">Scenes and sources in OBS.</span>

*Camera Left*I use this one for games that have little information in the lower
right corner.

*Camera Right*I use this one for games that have little information in the lower
left corner.

*Mini-game*This makes my camera the full size of the screen and reduces the game
to a smaller overlay size. If I am talking a lot or waiting for a game to load I
can switch to this one for a break in the stream without losing context of what
I’m doing.

*BRB*I use this screen when I need a break. I keep many image sources in this
scene for different games I play so I can fire up the relevant BRB images.

![](https://cdn-images-1.medium.com/max/500/1*bAOYS66fBv_67uNsGGffDw.jpeg)

![](https://cdn-images-1.medium.com/max/500/1*0DbPjBR4nMovlHHEQJIw0w.jpeg)

![](https://cdn-images-1.medium.com/max/500/1*9EieHn8sxq5OkW3BpaLMVw.jpeg)
<span class="figcaption_hack">Some of my BRB screens for various games. I can still use the text tool in OBS
to overlay more information about when I will return.</span>

I also set up scenes for certain games that I’m playing a lot which allows me to
customize the layout specifically to the game’s UI.

Within scenes you can always toggle on or off a layer’s visibility by tapping
the eye icon. When I get a scene laid out properly, I like to lock all the
layers that I won’t be moving with the lock icon. This prevents me from screwing
up scenes inadvertently.

You can also set the transition that occurs between scenes in the ‘Transition’
panel. I generally find that a quick cross-fade works pretty well, but you can
also create more exciting animations. OBS even supports video stingers which
allow you to create totally custom transitions.

![](https://cdn-images-1.medium.com/max/1000/1*lJeCrykRIS-NVXIVqmOENA.png)
<span class="figcaption_hack">Chatty’s interface</span>

#### Chat

I tried out a bunch of chatbots for my chat but most of them are mainly useful
for very active chats. Something that did provide me immediate value is
[Chatty](http://chatty.github.io/) (Windows only). Chatty is so full of features
it’s hard to describe. Here’s how to set it up:

1.  Download [Chatty](http://chatty.github.io/#download) (standalone version) and
install on your machine.
1.  Log into your Twitch account through Chatty.
1.  Choose your channel name, which is your Twitch username and connect.
1.  Make sure to select ‘Rejoin Open Channels’ so whenever you open Chatty it will
reopen your chat.

Since I only have one monitor, I wanted to avoid switching in and out of my game
as much as possible. I set up notifications for new chat messages as well as
when people joined my chat
([tutorial](https://www.youtube.com/watch?v=7VsY6dBfI64)). I can see these
notifications over my game view and respond to them accordingly. I also added
sounds to certain notifications so I wouldn’t miss them.

![](https://cdn-images-1.medium.com/max/1000/1*bXGPV2GYmQ7EnlmAz299bQ.png)
<span class="figcaption_hack">My notification settings for Chatty.</span>

I also use Chatty’s Admin window to set up my stream information such as the
title, the game I’m playing and associated communities. I use the Info window to
keep track of how many viewers are in my stream over time. You can think of
Chatty as a native replacement for using the Twitch dashboard.

![](https://cdn-images-1.medium.com/max/1000/1*RnAUlJ8RzFZEtK3P1UaNYg.png)
<span class="figcaption_hack">Updating the channel info from Chatty.</span>

Chatty can do so much more: moderation support, highlighting certain viewers in
chat, and viewing all messages of a specific chatter. Play around with this one
and see what it can do for you.

#### Videos

You can use a ‘Media’ source to set up scenes of video playback. This can be
used to play intro, outro or transitioning video content in your stream.

![](https://cdn-images-1.medium.com/max/1000/1*Rd_gaIISVgSXNpUDhI9asw.jpeg)
<span class="figcaption_hack">Twitch Extensions</span>

#### Extensions

Twitch has a feature called [Extensions](https://www.twitch.tv/p/extensions/).
Developers can create extensions that you can enable on your stream. These
extension allow interactions or display of data. For example, a viewer can look
at your Destiny 2 loadout with the [Destiny 2 Armory
Overlay](https://blog.twitch.tv/show-what-your-guardian-is-made-of-with-the-destiny-2-armory-overlay-238eaba9009f).

#### Profile

Another important experience to consider is your profile. People might come
across your stream but not be sure why they should care about you. Indulge them
with some good information to sink their teeth into.

I include an *about *section, games I am currently playing, my friends who also
stream, other social profiles and information about my setup. I’d err on the
side of overindulgence rather than being shy. People are looking at this area to
find out more about you, give it to them.

![](https://cdn-images-1.medium.com/max/1250/1*56P73_LqEqgU6uIJE_1CzQ.png)
<span class="figcaption_hack">Some of the information on my profile. The units on the right layout according
to the available space.</span>

You can customize the look of this section by creating graphics. There are tons
of [pre-made
templates](https://www.behance.net/gallery/28221943/FREE-Twitch-Panel-Theme-Pack)
out there if you are overwhelmed by that task, but I think it’s pretty fun to
create your own to match the visuals in your stream.

It’s also important to consider the experience of your channel when you are not
streaming. I recommend going to your ‘Channel & Video’ settings and auto-hosting
your friends or other streamers you enjoy. They might even auto-host you back.

In the case that no one you are hosting is streaming you can also set up a
custom Video Player Banner. This is also in your ‘Channel & Video’ settings and
it is a 16:9 image that is shown in the spot of the video player when you are
not online.

![](https://cdn-images-1.medium.com/max/1250/1*vcVTfhRz5slgSDsoBpHWJg.png)
<span class="figcaption_hack">What my video player looks like when I’m away.</span>

### 3. Viewership

Everyone says getting a streaming audience is real hard. I am in no way an
expert about this since I haven’t built much of an audience beyond my friends
yet, but here are the tips I’ve heard researching what other people have to say
about the topic:

#### Keep talking

It feels very awkward to [keep
talking](https://www.youtube.com/watch?v=tQ-HabUlqQw) even when no one is
watching but it’s actually really important. Someone can jump into your stream
and see you sitting around quietly staring at your screen and leave right away.
This might happen before you even get notified that someone is there.

If you are talking and they jump in, they will get a better sense of who you are
and may be compelled to stick around a while longer. People say once you get
used to this stream of consciousness it becomes easy. I really enjoy the
challenge of thinking that way and I think it will give me more confidence in
speaking in general if I can get good at it.

#### Socialize

Meet other like-minded streamers. Get to know them. Learn from them. Streaming
is a community just like any other community and people want to help and learn
from each other.

![](https://cdn-images-1.medium.com/max/1000/1*N-T9YVM4RI545DYQZZJciA.png)
<span class="figcaption_hack">Discord — ‘Streamer Mode’ automatically turns on when using OBS.</span>

#### Discord

If you are playing with friends, ask them if you can include their
[Discord](https://discordapp.com/) audio in your stream.

One issue I’ve already noticed is the awkwardness that can occur when responding
to your Twitch chat while being in a voice channel with your friends. I got a
tip from my friend [Hauz](https://www.twitch.tv/hauz) to set up a universal hot
key for muting your mic in Discord.

![](https://cdn-images-1.medium.com/max/1000/1*aqa0fi3jVRFQV2FUSfvCJQ.png)
<span class="figcaption_hack">Custom keybinds in Discord</span>

I set up Control-Shift-2 to mute my Discord mic, so when I want to respond to
someone on the stream I hold those keys down. You can obviously set up a simpler
quick key but I liked keeping my left hand in the same position as when I’m
gaming.

#### Multistream

Now that you are excited about streaming, maybe some of your friends also got
excited about streaming, and now the rest of your friends don’t know who to
watch since everyone is streaming. [Multistream](https://multistre.am/) lets you
create layouts of multiple streams at once. You can share a custom link and let
people view the action from multiple angles.

### Wrap-up

I hope this information helps you get started with streaming on Twitch. It’s
such an enjoyable process to customize your stream and profile once you get past
the technical hurtles and find the right tools.

If you’d like to watch my stream or just hang out, you can follow me at
[twitch.tv/gargarbot](https://www.twitch.tv/gargarbot). I’ve been streaming
games like PUBG, Overwatch, Destiny 2, and older classics like Mass Effect 2.
I’m also going to try dabbling in doing some game level design live in Unity and
Unreal Engine.