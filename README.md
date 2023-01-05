# Picture-In-Picture

> a simple Picture-In-Picture app

```js
// Prompt to select media stream, pass to video element, then play
async function selectMediaStream() {
  try {
    const mediaStream = await navigator.mediaDevices.getDisplayMedia();
    videoElement.srcObject = mediaStream;
    videoElement.onloadedmetadata = () => {
      videoElement.play();
    };
  } catch (error) {
    // Catch error here
  }
}
```

The `requestPictureInPicture` method does not seem to be working anymore. It is however listed in the documentation so the issue may be on my end. 
