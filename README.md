# Group-4-Finals-Face-Recognition-
![image](https://github.com/Jerrold026/face_recognition/assets/143669000/551837e7-42b2-4aaa-8715-ffb90178df97)

✅Engineering is the application of science and mathematics to solve problems. Engineers figure out how things work and find practical uses for scientific discoveries. Scientists and inventors often get the credit for innovations that advance the human condition, but it is engineers who are instrumental in making those innovations available to the world.
In his book, "Disturbing the Universe" (Sloan Foundation, 1981), physicist Freeman Dyson wrote, "A good scientist is a person with original ideas. A good engineer is a person who makes a design that works with as few original ideas as possible. There are no prima donnas in engineering."
The history of engineering is part and parcel of the history of human civilization. The Pyramids of Giza, Stonehenge, the Parthenon and the Eiffel Tower stand today as monuments to our heritage of engineering. Today's engineers not only build huge structures, such as the International Space Station (ISS), but they are also building maps to the human genome and better, smaller computer chips.


✅Face recognition is a method of identifying or verifying the identity of an individual using their face. Face recognition systems can be used to identify people in photos, video, or in real-time. Law enforcement may also use mobile devices to identify people during police stops. But face recognition data can be prone to error, which can implicate people for crimes they haven’t committed. Facial recognition software is particularly bad at recognizing African Americans and other ethnic minorities, women, and young people, often misidentifying or failing to identify them, disparately impacting certain groups.Additionally, face recognition has been used to target people engaging in protected speech. In the near future, face recognition technology will likely become more ubiquitous. It may be used to track individuals’ movements out in the world like automated license plate readers track vehicles by plate numbers. Real-time face recognition is already being used in other countries and even at sporting events in the United States. 


✅!git clone https://github.com/Jerrold026/face_recognition.git:
This command clones (downloads) a Git repository from the URL provided (https://github.com/Jerrold026/face_recognition.git). It creates a local copy of the repository in your current directory.

✅!pip install face_recognition:
This command uses pip (Python's package installer) to install the face_recognition library. This library provides functionalities for face recognition in Python.

![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/7e992050-4b9c-4435-856f-f01ebb0ee775)

✅The code below is creating encoding profiles for facial recognition using the face_recognition library in Python. It loads images of five different individuals, encodes their facial features, and creates a database of known faces for identification purposes.

✅Image Loading: The code loads images (like "elon.jpeg", "henry ford.jpeg", etc.) of notable figures using the face_recognition.load_image_file function.

✅Feature Encoding: For each image, it computes facial encodings—numerical representations of unique facial features—using face_recognition.face_encodings. These encodings are numerical arrays that represent distinct facial characteristics.

✅Database Creation: The encoded facial features are stored in lists (known_face_encodings) alongside corresponding names (known_face_names). These lists serve as a reference database for recognizing known individuals.

✅Identification Labels: The names provided ("Elon Musk," "Henry Ford," etc.) are associated with the encoded facial features, acting as labels for identification.

✅Recognition System: This sets the foundation for a facial recognition system, where these known faces can be compared against other faces to identify and label individuals in images or video frames based on their facial features.
![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/cf6b1263-1b68-4191-9cc9-e457bbf52604)

This code below analyzes an "unknown_em.jpeg" image using facial recognition techniques with the `face_recognition` library and OpenCV in Python.

✅ **Image Loading:** It loads the "unknown_em.jpeg" image and prepares it for analysis using `face_recognition.load_image_file` and `cv2.imread`.

✅**Face Detection:** The code identifies face locations within the unknown image using `face_recognition.face_locations`.

✅**Encoding Faces:** Facial encodings for these detected face locations are computed using `face_recognition.face_encodings`.

✅**Comparison and Identification:** It compares the unknown face encodings against the known faces' encodings using `face_recognition.compare_faces`. If a match is found, it assigns a name to the recognized face based on the closest match in the known face database and if not is display unknown. 

✅**Visual Representation:** For each recognized face, the code draws a rectangle around the face and labels it with the recognized individual's name using OpenCV's `cv2.rectangle` and `cv2.putText` functions, providing a visual representation of the identified faces in the image.

![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/9139f9b5-bd05-4923-a147-06045454b969)

✅**Description of Elon Musk:**

Elon Musk (born June 28, 1971 in Pretoria, South Africa) is a South African-born American entrepreneur who co-founded PayPal and SpaceX, a producer of launch vehicles and spacecraft. He was also one of the first important investors in and the CEO of the electric automobile business Tesla. Furthermore, Musk acquired Twitter (later X) in 2022.

![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/ba71c98b-cc07-497e-a760-8eeb1394ecc3)

✅**Description of Henry Ford:**

Henry Ford (1863-1947) built his first gasoline-powered horseless carriage, the Quadricycle, in the shed outside his house while working as an engineer for the Edison Illuminating Company in Detroit. To meet overwhelming demand for the revolutionary vehicle, Ford introduced revolutionary new mass-production methods, including large production plants, the use of standardized, interchangeable parts, and the world's first moving assembly line for cars in 1913. Ford, who had enormous power in the industrial world, was also an ardent political figure. During the early years of World War I, Ford faced criticism for his pacifist stance, as well as for his anti-Semitic ideas and writings.

![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/5bc11914-a482-4851-ae90-820626f6b78d)

✅**Description of Nikola Tesla:**

Nikola Tesla was an engineer and scientist best known for developing the alternating-current (AC) electric system, which is still the most common electrical system in use today. In addition, he invented the "Tesla coil," which is still utilized in radio technology today. Tesla, who was born in modern-day Croatia, immigrated to the United States in 1884 and briefly collaborated with Thomas Edison before the two parted ways. He sold various patent rights to George Westinghouse, including those to his AC machinery.

![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/cfd6bc8c-c041-4050-9a08-b1af56882bc2)

✅**Description of Lucio Tan:**

Lucio Tan (born July 17, 1933 in Amoy, Fujian Province, China) is a Chinese-born Filipino businessman who founded Fortune Tobacco Corp., Asia Brewery, Inc., and Philippine Airlines, Inc. Tan was the oldest of eight siblings. Far Eastern University in Manila was where he studied chemical engineering. He began his career as a janitor in a cigarette factory before being promoted to tobacco "cook," in charge of monitoring the product mix. Tan founded his own tobacco company, Fortune Tobacco Corp., in 1966.

![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/7d0313fe-7032-4b51-85cb-935b8bb5aacf)

✅**Description of Ramon Ang:**

Ramon See Ang (RSA) is a Filipino businessman who was born on January 14, 1954. He is the president and chief executive officer (CEO) of Top Frontier Investment Holdings, Inc., San Miguel Corporation's largest stakeholder. He is also the chairman of Cyber Bay Corporation and Eagle Cement Corporation, as well as the president and CEO of SMC. In January 1999, Ang was appointed vice-chairman of SMC, and in March 2002, he was named president and chief operating officer (COO). In June 2012, he took over SMC by purchasing the shares of Eduardo Cojuangco, Jr., a fellow Filipino businessman and politician. SMC changed its by-laws on April 15, 2021, ten months after Cojuangco's death, to merge the role, functions, and duties of the CEO with those of the president. According to the PSE declaration following SMC's 2021 annual stockholders' meeting, Ang retains the company's vice-chairman, president (CEO), and COO. Far Eastern University awarded Ang a Bachelor of Science in mechanical engineering.

✅**Ten Image for the Unknown Faces:**
![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/f362a9fe-0548-4034-accd-fcd7d080ffb0)
![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/7ef9e90c-9090-4f92-a4c8-9b0a7ebbfa06)
![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/85d4d3fd-b536-4c85-9e8b-5437a523a676)
![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/5d0c9feb-efde-477f-9ac2-65676d53337f)
![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/a118c1cc-8ee9-47f8-917e-261c8cccf2b0)
![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/fc17dce3-32f1-4ee5-a4c6-8dab2d021100)
![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/f4afca99-efa5-47e7-8a35-a20edcc3db83)
![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/ae690d5a-c072-43cb-beb2-552a5ff52b2d)
![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/7800a7a7-4952-4fba-9f6f-1907ee8c28c3)
![image](https://github.com/Jerrold026/Group-4-FInals-Face-Recognition-/assets/143669000/26b439b3-1374-4148-8c44-655443cb321f)


𝐒𝐎𝐔𝐑𝐂𝐄𝐒:
Green, A. (2010, June 16). Lucio Tan | Business, Biography, & Facts. Encyclopedia Britannica. https://www.britannica.com/biography/Lucio-Tan

Gregersen, E. (2023, December 10). Elon Musk | Biography, SpaceX, Tesla, Twitter, X, & Facts. Encyclopedia Britannica. https://www.britannica.com/biography/Elon-Musk

https://dbpedia.org/page/Ramon_Ang

Henry Ford - Biography, Inventions & Assembly Line. (2009, November 9). HISTORY. https://www.history.com/topics/inventions/henry-ford

Lucas, J., & Dobrijevic, D. (2022, February 28). What is engineering? livescience.com. https://www.livescience.com/47499-what-is-engineering.html

Nikola Tesla. (2023, March 7). Biography. https://www.biography.com/inventors/nikola-tesla








 



