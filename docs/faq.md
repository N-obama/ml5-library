this is not a question i just did not know how to feedback, i think ml5.facemesh has a problem, when i call it, it shows error: 
"Uncaught TypeError: Cannot read property 'split' of undefined (: line 57)"

that's code, if something is wrong with it(i am using ml5 version 0.6.0:

var vid;
function preload () {
  vid = createCapture (VIDEO);
}

function draw () {
  background (51);
  image (vid, 0, 0);
  
  if (pred.length)
    console.log (pred.length);
  
}

let pred = [];

const f = ml5.facemesh(vid, modelLoaded);
function modelLoaded() {
  console.log('Model Loaded!');
}

f.on('predict', results => {
  pred = results;
});
