# Face Recognition

### Using haarcascade_frontalface_default

```sh
face_cascade = cv2.CascadeClassifier("../detector_architectures/haarcascade_frontalface_default.xml")
faces = face_cascade.detectMultiScale(gray, 4, 6)
```

### Copy the image and write rectangle on faces
```sh
image_detector = np.copy(image_copy)

for (x, y, w, h) in faces:
    cv2.rectangle(image_detector, (x, y), (x+w, y+h), (255, 0, 0), 5)
    
plt.figure(figsize=(20, 10))
plt.imshow(image_detector)
```

![ss4](https://user-images.githubusercontent.com/47830409/63946247-7ab64880-ca7d-11e9-8f07-1f31f8148f86.PNG)
