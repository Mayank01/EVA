## Face Processing, General Tracking and Stabilization

### Many Use Cases:

>1. Landmark Detection
>2. Tracking
>3. Augmented Reality
>4. Emotion Recognition
>5. Authentication
>6. Facial Filters
>7. Computational Photography
>8. Facial Portraits
>9. Photo Enhancement
>10. Virtual Makeover (shooting photos of models with different makeup is expensive and time consuming (virtual hairstyle) https://www.youtube.com/watch?v=PksoH8gJQFA
>11. Virtual Sunglasses
>12. Virtual Jewellery
>13. Virtual output of plastic surgery

## Assignment:

#### Implement the following:
> Use dlib Face Detector 
1. Align the face using 5-pt detector and align (take a 5 second video of your face with some translation and rotation (not extreme)
2. Calculate 68-pt landmark on the aligned faces
3. Calculate the optical flow for these 68-pts every frame
4. Stabilize the optical flow using LK method as we discussed. 
5. Create a 5 second video, with three windows:
>1. First: Original frame
>2. Aligned Frame with unstabilized points
>3. Aligned Frame with stabilzed points. 
>4. If the original video was 400x400 resolution, final video is 1200x400. Final video is 5 seconds and we need to see all 3 videos side by side for comparison. 
6. Upload to youtube, and embed the video in your readme file. 
7. Share the link. 
