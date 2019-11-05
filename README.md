# Video Doorbell, Lab 7

*A lab report by John Q. Student*

### In This Report

1. Upload a video of your version of the camera lab to your lab Github repository
1. As usual, update your class Hub repository to add your [forked IDD-Fa18-Lab7](/FAR-Lab/IDD-Fa18-Lab7) repository.
1. Answer the questions in-line below on your README.md.

## Part A. HelloYou from the Raspberry Pi

**a. Link to a video of your HelloYou sketch running.**  
[Video](https://youtu.be/fH7V6s5b2zA)

## Part B. Web Camera

**a. Compare `helloYou/server.js` and `IDD-Fa18-Lab7/pictureServer.js`. What elements had to be added or changed to enable the web camera? (Hint: It might be good to know that there is a UNIX command called `diff` that compares files.)**  
add `takePicture();` to the code.    

**b. Include a video of your working video doorbell**  
[Video](https://youtu.be/_tBfAM__2ok)

## Part C. Make it your own

**a. Find, install, and try out a node-based library and try to incorporate into your lab. Document your successes and failures (totally okay!) for your writeup. This will help others in class figure out cool new tools and capabilities.**  
I used google cloud vision api[https://www.npmjs.com/package/@google-cloud/vision] to add tag to the object in the image.  
```
async function quickstart() {
  // Imports the Google Cloud client library
  const vision = require('@google-cloud/vision');
 
  // Creates a client
  const client = new vision.ImageAnnotatorClient();
 
  // Performs label detection on the image file
  const [result] = await client.labelDetection('./resources/wakeupcat.jpg');
  const labels = result.labelAnnotations;
  console.log('Labels:');
  labels.forEach(label => console.log(label.description));
}
```

**b. Upload a video of your working modified project**  
[Video](https://youtu.be/aO6K_AUvuSI)
