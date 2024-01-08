---
title: "Syncing Across Tabs: The JavaScript Magic You Didn't Know Existed!"
datePublished: Sat Jan 06 2024 18:49:07 GMT+0000 (Coordinated Universal Time)
cuid: clr2f5e53000009juctlo5s0n
slug: syncing-across-tabs-the-javascript-magic-you-didnt-know-existed
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1704566592592/97090d0d-d59d-40e2-b083-9034bb4366a0.png
tags: javascript, webdev

---

I recently discovered a fascinating feature on the [SoundCloud](https://soundcloud.com/) website: the ability to seamlessly control audio playback across multiple tabs in the same browser. Intrigued by this, I delved into how it was implemented and stumbled upon a powerful tool - JavaScript's [Broadcast Channel API](https://developer.mozilla.org/en-US/docs/Web/API/Broadcast_Channel_API).

The Broadcast Channel API allows communication between browser tabs, making real-time updates and synchronization possible. It's supported by major browsers, making it a versatile solution for enhancing user experiences.

## Using the Broadcast Channel API

To implement this feature, create a `BroadcastChannel` object with a channel name, like so:

```ts
const broadCast = new BroadcastChannel('audio-player');
```

Now, you can send messages using postMessage:

```ts
broadCast.postMessage({
    type: 'audio-played',
});
```

To receive messages, subscribe to the onmessage event:

```ts
broadCast.onmessage = ({ data = {} }) => {
    console.log(data);
};
```

This simple yet powerful API enables real-time communication between browser tabs, opening up possibilities for dynamic and synchronized user interfaces.

I have created a sample demo to showcase this feature.

* [Source Code](https://github.com/bhumit070/browser_tabs_communication)
    
* [Live Demo](https://bhumit070.github.io/browser_tabs_communication/)
    

## Conclusion

The Broadcast Channel API offers a seamless solution for enhancing multi-tab support on your website. Explore this feature in your projects and unlock the potential for dynamic and synchronized user experiences.

## Follow me for more updates

* [Twitter](https://twitter.com/bhumit070)
    
* [Linkedin](https://www.linkedin.com/in/bhoomit-ganatra/)