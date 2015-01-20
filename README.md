# mnist.js
javascript MNIST library

----------------
How to use
----------------
//create mnist object
var mnist = Mnist({
    trainCount: 60000,                     // integer (60000 is max and also default value)
    testCount: 10000,                      // integer (10000 is max and also default value)
    trainImageFile: trainImageFileObject,  // file object
    trainLabelFile: trainLabelFileObject,  // file object
    testImageFile: testImageFileObject,    // file object
    testLabelFile: testLabelFileObject,    // file object
    LoopIncrementCountOfEachTimeout: 10,   // integer (If you want to calc fast, set bigger value. 1 to 60000) 
});

//start train and test
mnist.start(
    onTrainImageRead,         // function(index, label, imageData)
    onTestImageRead           // function(index, label, imageData)
);
"onTrainImageRead" and "onTestImageRead" is callback function. And these function have 3 parameters.



"index" is loop index.
"label" is teacher value.
"imageData" is 28*28 array, and each cell has 0 to 255 value.
