# "Streaming vs Downloading" Animation

I needed a quick animation to illustrate the differences between "streaming" and "downloading"; or rather, to illustrate their similarities.
Both involve all of the data in a media stream being sent from the server to the client.

The single biggest significant difference is that streaming implies that the frames of the media will be consumed as-they-arrive (or soon
after, when they reach the front of the buffer) and subsequently discarded, while downloading implies that the media won't be consumed until
it's fully-downloaded (although this does not have to be the case) and will be retained in a file afterwards.

There are, of course, other differences. Principal among them is the fact that a downloading client may well not care about the order in
which parts of the resulting media file are received (it can piece them together after-the-fact), a streaming client absolutely does care.
This difference in turn leads to potentially-different compression and/or encryption algorithms being used.

But the bottom line is that streaming and downloading can, in some cases, be indistinguishable from the server's perspective in a majority
of cases. When you view a video on the Web, the server asks and expects that you're going to "stream" it - that is, that you're not going
to retain a copy for later consumption - but there's no way that the server can be certain that this will be the case. Even where some
DRM solution is employed the server cannot be certain that what's happening is "streaming" and not "downloading", because even if the DRM
is bulletproof (which is, as we know, never the case indefinitely) the "analogue hole" can always be exploited.

## Making the animation

The animation is produced using CSS and a tiny bit of JavaScript. To see it in action, open `index.html` and press any key. It expects that
you have the font 'Raleway' installed locally.

## Producing the video

A pre-made `.mp4` version is available to stream (or download, now you know the difference!). This was produced by running OBS Studio against
a web browser viewing the above animation, recording at 60fps. It's intended for looping in a silent `<video>` element.

## License

The code used to produce the animation, the images, and the resulting video file are all released into the Public Domain or under a CC0
license; your choice. No attribution or payment is necessary to use any of these resources for any purpose, but I hope you'll use them
for educational purposes.

The "horse" images are from Eadweard Muybridge's "The Horse in Motion" series; they show Sallie Gardner being ridden by G. Domm in June 1878,
and are in the public domain. All the SVG images are CC0-licensed and were retreieved from SVGRepo.com; some have been modified from their
originals.
