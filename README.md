# Group-4-Finals-Face-Recognition-
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/551837e7-42b2-4aaa-8715-ffb90178df97)


<div align="justify">
✅Engineering is the application of science and mathematics to solve problems. Engineers figure out how things work and find practical uses for scientific discoveries. Scientists and inventors often get the credit for innovations that advance the human condition, but it is engineers who are instrumental in making those innovations available to the world.
In his book, "Disturbing the Universe" (Sloan Foundation, 1981), physicist Freeman Dyson wrote, "A good scientist is a person with original ideas. A good engineer is a person who makes a design that works with as few original ideas as possible. There are no prima donnas in engineering."
The history of engineering is part and parcel of the history of human civilization. The Pyramids of Giza, Stonehenge, the Parthenon and the Eiffel Tower stand today as monuments to our heritage of engineering. Today's engineers not only build huge structures, such as the International Space Station (ISS), but they are also building maps to the human genome and better, smaller computer chips.



✅Face recognition is a method of identifying or verifying the identity of an individual using their face. Face recognition systems can be used to identify people in photos, video, or in real-time. Law enforcement may also use mobile devices to identify people during police stops. But face recognition data can be prone to error, which can implicate people for crimes they haven’t committed. Facial recognition software is particularly bad at recognizing African Americans and other ethnic minorities, women, and young people, often misidentifying or failing to identify them, disparately impacting certain groups.Additionally, face recognition has been used to target people engaging in protected speech. In the near future, face recognition technology will likely become more ubiquitous. It may be used to track individuals’ movements out in the world like automated license plate readers track vehicles by plate numbers. Real-time face recognition is already being used in other countries and even at sporting events in the United States. 
</div>

<div align="justify">
✅!git clone https://github.com/Jerrold026/face_recognition.git:
This command clones (downloads) a Git repository from the URL provided (https://github.com/Jerrold026/face_recognition.git). It creates a local copy of the repository in your current directory.

✅!pip install face_recognition:
This command uses pip (Python's package installer) to install the face_recognition library. This library provides functionalities for face recognition in Python.
</div>

```
!git clone https://github.com/Jerrold026/face_recognition.git
!pip install face_recognition
%cd face_recognition
```


✅The code below is creating encoding profiles for facial recognition using the face_recognition library in Python. It loads images of five different individuals, encodes their facial features, and creates a database of known faces for identification purposes.

✅Image Loading: The code loads images (like "elon.jpeg", "henry ford.jpeg", etc.) of notable figures using the face_recognition.load_image_file function.

✅Feature Encoding: For each image, it computes facial encodings—numerical representations of unique facial features—using face_recognition.face_encodings. These encodings are numerical arrays that represent distinct facial characteristics.

✅Database Creation: The encoded facial features are stored in lists (known_face_encodings) alongside corresponding names (known_face_names). These lists serve as a reference database for recognizing known individuals.

✅Identification Labels: The names provided ("Elon Musk," "Henry Ford," etc.) are associated with the encoded facial features, acting as labels for identification.

✅Recognition System: This sets the foundation for a facial recognition system, where these known faces can be compared against other faces to identify and label individuals in images or video frames based on their facial features.



```
import face_recognition
import numpy as np
from google.colab.patches import cv2_imshow
import cv2

# Creating the encoding profiles
face_1 = face_recognition.load_image_file("elon.jpeg")
face_1_encoding = face_recognition.face_encodings(face_1)[0]

face_2 = face_recognition.load_image_file("henry ford.jpeg")
face_2_encoding = face_recognition.face_encodings(face_2)[0]

face_3 = face_recognition.load_image_file("nikola.jpeg")
face_3_encoding = face_recognition.face_encodings(face_3)[0]

face_4 = face_recognition.load_image_file("lucio tan.jpeg")
face_4_encoding = face_recognition.face_encodings(face_4)[0]

face_5 = face_recognition.load_image_file("ramon ang.jpeg")
face_5_encoding = face_recognition.face_encodings(face_5)[0]

known_face_encodings = [
                        face_1_encoding,
                        face_2_encoding,
                        face_3_encoding,
                         face_4_encoding,
                         face_5_encoding
]

known_face_names = [
                    "Elon Musk",
                    "Henry Ford",
                    "Nikola Tesla",
                    "Lucio Tan",
                    "Ramon Ang"

 ]
```


<div align="justify">
The code below analyzes an "unknown_em.jpeg" image using facial recognition techniques with the `face_recognition` library and OpenCV in Python.

✅ **Image Loading:** It loads the "unknown_em.jpeg" image and prepares it for analysis using `face_recognition.load_image_file` and `cv2.imread`.

✅**Face Detection:** The code identifies face locations within the unknown image using `face_recognition.face_locations`.

✅**Encoding Faces:** Facial encodings for these detected face locations are computed using `face_recognition.face_encodings`.

✅**Comparison and Identification:** It compares the unknown face encodings against the known faces' encodings using `face_recognition.compare_faces`. If a match is found, it assigns a name to the recognized face based on the closest match in the known face database and if not is display unknown. 

✅**Visual Representation:** For each recognized face, the code draws a rectangle around the face and labels it with the recognized individual's name using OpenCV's `cv2.rectangle` and `cv2.putText` functions, providing a visual representation of the identified faces in the image.
</div>

 ## ✅Famous Engineers - CEO

 ![Brown and Pink Minimalist Romantic Photo Collage](https://github.com/Jerrold026/face_recognition/assets/143669000/de8a5e96-dbec-4b9f-af46-387fac0530fa)
✅**Elon Musk:**
```
file_name = "unknown_em.jpeg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -30), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/ccbdf7f7-2afd-4017-ae22-0d13eec7db35)

           

<div align="justify">
Elon Musk (born June 28, 1971 in Pretoria, South Africa) is a South African-born American entrepreneur who co-founded PayPal and SpaceX, a producer of launch vehicles and spacecraft. He was also one of the first important investors in and the CEO of the electric automobile business Tesla. Furthermore, Musk acquired Twitter (later X) in 2022.
</div>

✅**Henry Ford:**
```
file_name = "unknown_he.jpeg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -40), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/485a5e7c-966c-4a69-9353-45387b8f718c)


<div align="justify">
Henry Ford (1863-1947) built his first gasoline-powered horseless carriage, the Quadricycle, in the shed outside his house while working as an engineer for the Edison Illuminating Company in Detroit. To meet overwhelming demand for the revolutionary vehicle, Ford introduced revolutionary new mass-production methods, including large production plants, the use of standardized, interchangeable parts, and the world's first moving assembly line for cars in 1913. Ford, who had enormous power in the industrial world, was also an ardent political figure. During the early years of World War I, Ford faced criticism for his pacifist stance, as well as for his anti-Semitic ideas and writings.
</div>


✅**Nikola Tesla:**

```
file_name = "unknown_ni.jpeg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -30), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```

![image](https://github.com/Jerrold026/face_recognition/assets/143669000/edf3241f-651d-424f-abd6-61a7eab1bc86)

<div align="justify">
Nikola Tesla was an engineer and scientist best known for developing the alternating-current (AC) electric system, which is still the most common electrical system in use today. In addition, he invented the "Tesla coil," which is still utilized in radio technology today. Tesla, who was born in modern-day Croatia, immigrated to the United States in 1884 and briefly collaborated with Thomas Edison before the two parted ways. He sold various patent rights to George Westinghouse, including those to his AC machinery.
</div>



✅**Lucio Tan:**

```
file_name = "unknown_lu.jpeg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -30), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/98994561-8f28-4621-a2dc-c4943d42a0c7)


<div align="justify">
Lucio Tan (born July 17, 1933 in Amoy, Fujian Province, China) is a Chinese-born Filipino businessman who founded Fortune Tobacco Corp., Asia Brewery, Inc., and Philippine Airlines, Inc. Tan was the oldest of eight siblings. Far Eastern University in Manila was where he studied chemical engineering. He began his career as a janitor in a cigarette factory before being promoted to tobacco "cook," in charge of monitoring the product mix. Tan founded his own tobacco company, Fortune Tobacco Corp., in 1966.
</div>

✅**Ramon Ang:**


```
file_name = "unknown_ra.jpeg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -40), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/73a91d1c-e7a4-48a4-aaf6-f0e4ea769577)


<div align="justify">
Ramon See Ang (RSA) is a Filipino businessman who was born on January 14, 1954. He is the president and chief executive officer (CEO) of Top Frontier Investment Holdings, Inc., San Miguel Corporation's largest stakeholder. He is also the chairman of Cyber Bay Corporation and Eagle Cement Corporation, as well as the president and CEO of SMC. In January 1999, Ang was appointed vice-chairman of SMC, and in March 2002, he was named president and chief operating officer (COO). In June 2012, he took over SMC by purchasing the shares of Eduardo Cojuangco, Jr., a fellow Filipino businessman and politician. SMC changed its by-laws on April 15, 2021, ten months after Cojuangco's death, to merge the role, functions, and duties of the CEO with those of the president. According to the PSE declaration following SMC's 2021 annual stockholders' meeting, Ang retains the company's vice-chairman, president (CEO), and COO. Far Eastern University awarded Ang a Bachelor of Science in mechanical engineering.
</div>


### ✅**Ten Unknown Engineers:**
![Brown and Pink Minimalist Romantic Photo Collage (1)](https://github.com/Jerrold026/face_recognition/assets/143669000/1444f61b-0720-4696-bc84-60e135bf4909)

```
file_name = "unknown_gs.jpeg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -20), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/c586d6d1-3d94-44f4-85d2-749d6aa33ed7)

```
file_name = "unknown_ed.jpg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -20), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/5fe198b2-0bc6-4147-b7d6-6cf8d3dd5dca)

```
file_name = "unknown_ja.jpg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -20), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/b29c02de-c237-44e1-9a7c-2240671271be)

```
file_name = "unknown_fr.jpg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -20), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/a1a38cc3-f7a4-4f07-829d-dc1a31d2dd5a)

```
file_name = "unknown_da.jpg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -20), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/380770bc-0e94-46f5-b08b-88b75d50ce5c)

```
file_name = "unknown_er.jpg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -20), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/c42b7aae-ef3d-4d9a-8312-9ff26f2f2723)

```
file_name = "unknown_mi.jpg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -20), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/3fa93544-d782-4575-bb6c-14fbf29e245e)

```
file_name = "unknown_to.jpg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -20), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/5e59a853-7177-4c05-b370-f36fc132dd81)

```
file_name = "unknown_sa.jpg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -20), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/f61a64b9-00ac-403c-86b6-5d5f5db9f04c)

```
file_name = "unknown_ti.jpg"
unknown_image = face_recognition.load_image_file(file_name)
unknown_image_to_draw = cv2.imread(file_name)

face_locations = face_recognition.face_locations(unknown_image)
face_encodings = face_recognition.face_encodings(unknown_image, face_locations)

for (top,right, bottom, left), face_encoding in zip(face_locations, face_encodings):
  matches = face_recognition.compare_faces(known_face_encodings, face_encoding)

  name = "Unknown"

  face_distances = face_recognition.face_distance(known_face_encodings, face_encoding)
  best_match_index = np.argmin(face_distances)
  if matches[best_match_index]:
    name = known_face_names[best_match_index]
  cv2.rectangle(unknown_image_to_draw, (left, top), (right, bottom),(0,220,0),3)
  cv2.putText(unknown_image_to_draw,name, (left, top -20), cv2.FONT_HERSHEY_SIMPLEX,0.5,(0,0,255),2, cv2.LINE_AA)

cv2_imshow(unknown_image_to_draw)
```
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/8f3314fc-109e-4a95-8976-c265214cb98e)



𝐒𝐎𝐔𝐑𝐂𝐄𝐒:


Green, A. (2010, June 16). Lucio Tan | Business, Biography, & Facts. Encyclopedia Britannica. https://www.britannica.com/biography/Lucio-Tan

Gregersen, E. (2023, December 10). Elon Musk | Biography, SpaceX, Tesla, Twitter, X, & Facts. Encyclopedia Britannica. https://www.britannica.com/biography/Elon-Musk

https://dbpedia.org/page/Ramon_Ang

Henry Ford - Biography, Inventions & Assembly Line. (2009, November 9). HISTORY. https://www.history.com/topics/inventions/henry-ford

Lucas, J., & Dobrijevic, D. (2022, February 28). What is engineering? livescience.com. https://www.livescience.com/47499-what-is-engineering.html

Nikola Tesla. (2023, March 7). Biography. https://www.biography.com/inventors/nikola-tesla








 



