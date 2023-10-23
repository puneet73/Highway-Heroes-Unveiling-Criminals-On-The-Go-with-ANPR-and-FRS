# anpr-and-frs
Advanced automatic number plate recognition (ANPR) and facial recognition system (FRS) solutions refer to the use of sophisticated technology to automatically capture and analyse vehicle licence plates and human faces, respectively. These systems use cameras and software to identify and match patterns, allowing for the quick and accurate identification of individuals and vehicles in various settings. ANPR and FRS solutions have a wide range of applications, from enhancing security and law enforcement to improving traffic management and public safety. However, current ANPR and FRS systems have several limitations and challenges that can be addressed through the development of advanced solutions, and our proposed solution aims to minimize these limitations and overcome these hurdles.

Advanced ANPR and FRS solutions are important technologies due to their potential applications in a wide range of settings, including law enforcement, transportation, and public safety. By automatically capturing and analysing vehicle license plates and human faces, these systems can provide valuable insights and help to solve crimes, improve traffic management, and enhance security. In law enforcement, ANPR and FRS systems can be used to identify suspects and locate missing persons quickly and accurately. They can also be used to monitor traffic violations and enforce traffic laws, helping to improve public safety on roads and highways. In transportation, ANPR systems can be used to manage traffic flow and monitor parking, while FRS systems can be used for security screening at airports and other transportation hubs. Moreover, ANPR and FRS systems have potential applications in the private sector, including in retail and entertainment venues, where they can be used to identify and track customers and provide personalised marketing and customer service. They can also be used in healthcare settings to verify patient identities and improve patient care. Overall, the potential applications of ANPR and FRS technology are diverse and wide-ranging, making them valuable tools for improving efficiency, enhancing security, and advancing public safety. However, there is still room for improvement in the accuracy and reliability of these systems, which can be addressed through the development of advanced ANPR and FRS solutions.


*ANPR LIMITATIONS*
While ANPR and FRS systems have proven to be valuable tools in a wide range of settings, there are still several challenges and limitations that need to be addressed. Some of the key issues with current ANPR and FRS systems include: 

Poor image quality: ANPR systems rely on clear and high-quality images to accurately identify number plates. However, poor lighting conditions, low resolution cameras, or blurred images can make it difficult for ANPR systems to accurately identify number plates.
Variation in number plate formats: Number plates can have different formats depending on the country, region, or even the type of vehicle. This variation can make it challenging for ANPR systems to accurately recognize number plates.
Computational load: ANPR systems need to process large amounts of data in real-time to identify number plates. This can lead to a high computational load and longer processing times.
Noise and variations in the image or video sequence: ANPR systems need to be able to recognize number plates even in situations where there is a lot of noise or variation in the image or video sequence.
False positives and false negatives: ANPR systems may sometimes incorrectly identify number plates, leading to false positives or false negatives. False positives can result in unnecessary alerts or actions, while false negatives can result in missed detections.

Improved ANPR and FRS systems are needed to address these challenges and limitations. By developing more accurate, reliable, and privacy-conscious systems, organisations and agencies can benefit from enhanced efficiency, improved security, and better public safety outcomes.


*ANPR Solution*

To improve the accuracy of current Automatic Number Plate Recognition (ANPR) systems, we use Convolutional Neural Networks (CNNs) followed by image quality enhancement. CNN can analyse number plates in a more comprehensive way. These networks are trained on large datasets of number plates, enabling them to learn and recognize number plate features and patterns in a more robust and accurate way.





Along with CNN ,for increasing the efficiency and reducing the total area scanned to capture the number plate we are using Template Matching .In Template matching using computer vision technique it is easy to identify a particular pattern or template within an image or a video frame. In the context of matching various types of number plates, template matching can be used to identify a specific number plate format by comparing it with a pre-defined templates.To perform template matching for number plates, a large database of templates, each of which corresponds to a specific number plate format, the system would analyse an incoming image or video frame of a number plate and compare it with the templates in the database to identify the closest match.The closeness of the image or video frame is measured using techniques such as pixel intensity matching, edge detection, feature extraction, and pattern recognition.Once a match has been found, the system can then extract relevant information from the number plate, such as the country code, registration number, and any other relevant data. This information can then be used for various purposes, such as vehicle tracking, law enforcement, or toll collection.
Template matching reduces the total scanned area of a vehicle when detecting its number plate because it allows for a more targeted search of the image or video frame.Instead of scanning the entire image or video frame for the number plate, template matching involves comparing a smaller area of the image with a predefined template of a number plate. If the comparison results in a match, then the system can conclude that the number plate is present in that area and can extract the relevant information.This approach reduces the computational load on the system, as it only needs to analyse a smaller portion of the image or video frame. It also improves the accuracy of number plate detection, as the system is searching for a specific pattern rather than trying to identify a number plate from a larger, more complex image.One advantage of this approach is that it can be used to detect a wide range of non-standard number plate formats, even if they are not recognized by traditional optical character recognition (OCR) algorithms. This is because template matching is based on a visual pattern recognition rather than character recognition.Another advantage is that the system can be trained to recognize new number plate formats by simply adding a new template to the database. This makes the system more flexible and adaptable to changing conditions or new requirements.

To overcome the noise and variations in the image or video sequence, we are using trained HMM(Hidden Markov Models).In the context of number plate detection, an HMM model can be trained to recognize the statistical patterns of different number plate formats. This involves training the model using a set of labelled data that contains the different number plate formats and the corresponding sequence of characters along with all the template databases to improve the accuracy and robustness of the system.
First, the system uses template matching to identify the location of the number plate in the image or video frame.Once the location of the number plate is identified, the system can use HMM to recognize the characters on the number plate.


However, video footage can be shaky, blurry, or have other issues that can make it difficult for ANPR algorithms to accurately recognize the license plates.
To address this issue, one technique is to divide the video into thousands of individual frames and then merge them together to create a clearer image of the license plate. This technique is similar to how astronomers use image stacking to create a clear image of celestial bodies.
In the case of ANPR, each frame of the video may capture a slightly different perspective or angle of the license plate due to camera movement or vibrations. By merging all of these frames together, the resulting image will have a higher signal-to-noise ratio, making it easier for ANPR algorithms to accurately recognize the license plate.
The process of merging frames involves aligning and combining each frame, so that the resulting image is a combination of the sharpest and clearest parts of each frame.

Advantages of merging multiple images : 
Noise Reduction: When multiple images of the same scene or object are captured, each image contains some noise due to various factors like sensor noise, atmospheric turbulence, or camera shake. By merging multiple images, the noise is reduced, and the resulting image has a higher signal-to-noise ratio. The mathematical aspect of this is that the noise in each image is random, and when multiple images are combined, the random noise cancels out, resulting in a cleaner image.
Dynamic Range Extension: Sometimes, the contrast between the brightest and darkest areas in a scene is too high for a single image to capture. By merging multiple images, the dynamic range can be extended, resulting in an image with more detail in the highlights and shadows. The mathematical aspect of this is that each image captures a different part of the scene's dynamic range, and by merging them, the full range of the scene can be captured.
Increased Resolution: When multiple images are merged, the resulting image can have a higher resolution than each individual image. This is because each image captures a slightly different part of the scene, and by merging them, the resulting image has more information. The mathematical aspect of this is that the information from each image can be combined using various techniques like interpolation, which results in a higher resolution image.
Elimination of Artifacts: When multiple images are merged, some artifacts like lens distortion or vignetting can be eliminated. The mathematical aspect of this is that the artifacts in each image are slightly different, and by merging them, the resulting image can have less distortion and vignetting.


Combining the results of multiple camera angles can further improve the accuracy of ANPR systems. This is achieved using multi-camera tracking. In this technique, multiple cameras are used to capture images of a vehicle from different angles. These images are then analyzed by the ANPR system to extract the number plate information. By combining the results from different cameras, the ANPR system can improve the accuracy of number plate detection and reduce false positives. In the context of ANPR systems, stereo matching is used to improve the accuracy of number plate detection by allowing the system to more accurately determine the position and orientation of the number plate in 3D space. This involves comparing the two or more images captured by the cameras and identifying corresponding points in each image. By analysing the differences between these corresponding points, the system can calculate the distance between the cameras and the objects in the scene. Once the system has calculated the depth information for the objects in the scene, it can use this information to more accurately locate the number plate on the vehicle. For example, the system could use the depth information to determine the position and orientation of the number plate relative to the cameras and then use this information to extract the number plate information more accurately.

C-SVMs are most commonly used in current ANPR systems. However, C-SVM has some limitations when it comes to handling non-linear data. In ANPR systems, license plates can have various shapes and sizes, and the lighting and weather conditions can also affect the quality of the images. These factors can make the data non-linear, which can lead to poor performance of C-SVM. On the other hand, radial SVM is a non-linear SVM that can handle non-linear data by transforming the data into a high-dimensional feature space. Radial SVM has been shown to perform better than C-SVM on non-linear data in various applications, including ANPR systems. Radial SVM can capture the non-linear patterns and variations in the license plate images, resulting in better recognition performance. Radial SVM can also handle the variations in lighting and weather conditions, which can affect the quality of the images.  Radial SVM can be trained on a large dataset of license plates to learn the patterns and variations in the data, resulting in better recognition performance. In conclusion, using radial SVM will be better than using C-SVM in ANPR systems.

Super-resolution algorithms and image enhancement techniques are used to improve the quality of CCTV feeds and enhance the accuracy of ANPR systems. Super-resolution algorithms aim to reconstruct a high-resolution image from a low-resolution image or sequence of images. These algorithms learn to map low-resolution images to high-resolution images by training on large datasets of paired low- and high-resolution images. Once trained, these models can be used to upscale low-resolution images to higher resolutions, resulting in improved image quality and better ANPR performance. Image enhancement techniques improve the visual quality of images by adjusting contrast, brightness, and sharpness, removing noise, and correcting color distortions. The techniques used are  histogram equalization, contrast stretching, and noise reduction. Histogram equalization adjusts the intensity levels of an image to improve contrast and highlight details. Contrast stretching adjusts the dynamic range of an image to enhance its visual appearance. Noise reduction techniques such as median filtering or wavelet denoising can be used to remove noise from images and improve their clarity. In addition to these techniques, image stabilization algorithms that compensate for camera motion and reduce blur are also used. These algorithms estimate the motion between frames and apply image warping to align the frames, resulting in a stabilized image sequence that can be used for ANPR. Overall, the use of super-resolution algorithms and image enhancement techniques significantly improve the accuracy of ANPR systems in CCTV feeds.

Although a lot of the above algorithms and models have been talked about in the context of ANPR systems, they apply to FRS systems as well. Coming to FRS systems in specific, they are made more accurate by employing deep learning algorithms, especially Convolutional Neural Networks (CNNs), which are adept at analyzing facial features. These networks are trained on extensive datasets of facial images, enabling them to learn and recognize facial features and patterns more accurately and robustly. Additionally, feature extraction techniques such as Local Binary Pattern (LBP) and Principal Component Analysis (PCA) can be utilized to extract the most distinctive features from facial images. These features can be used to train machine learning models such as Support Vector Machines (SVMs) to accurately classify and recognize faces. Furthermore, pre-trained models such as DeepFace and FaceNet are used to achieve high accuracy in face recognition. DeepFace, developed by Facebook, is a CNN-based model that is trained on over four million facial images, enabling it to recognize faces accurately under challenging conditions, including lighting and pose variations. FaceNet, developed by Google, uses a triplet loss function to learn embeddings of faces that accurately represent an individual's unique features, resulting in high accuracy in face recognition tasks. Consequently, by utilizing these technical approaches, more precise and efficient FRS systems can be developed. These systems can help law enforcement agencies identify and apprehend suspects, locate missing persons, and enhance public safety.

Our proposed solution addresses some of the main challenges and limitations in current ANPR and FRS systems. One of the primary challenges in ANPR (Automatic Number Plate Recognition) and FRS (Facial Recognition Systems) is the accuracy of the system in identifying the required information, especially in situations with poor image quality, occlusion or variation in the format of the number plates or facial features. The use of CNNs allows for more comprehensive analysis of number plates and robust recognition of facial features and patterns. This results in increased accuracy and improved performance of the ANPR and FRS system. Another challenge in ANPR and FRS is the computational load and time required to scan the entire image or video frame for the number plate. The use of template matching reduces the total scanned area of a vehicle and allows for a more targeted search of the image or video frame. This reduces the computational load on the system and improves the accuracy of number plate detection. Also as mentioned before, our solution addresses the issue of noise and variation in the image or video sequence by the use of HMM which allows for the recognition of statistical patterns of different number plate formats and faces, which results in improved accuracy and robustness of the system. Overall, the proposed solution utilises advanced machine learning techniques to improve the accuracy, efficiency, and robustness of ANPR systems, addressing some of the main challenges and limitations in current ANPR and FRS systems.

Our proposed software-based solution has a wide range of potential real-world applications, particularly in the fields of law enforcement, transportation, and security. Some of the potential applications of our solution include: 

Law Enforcement: Our solution can be used by law enforcement agencies to enhance their surveillance capabilities and improve their ability to track vehicles and individuals of interest. This can be particularly useful in investigations of criminal activity, including drug trafficking, organized crime, and terrorism. 
Transportation: Our solution can be used by transportation authorities to improve traffic flow and monitor vehicle movement in real-time. This can be particularly useful for toll collection, parking enforcement, and managing congestion on highways and city streets. 
Security: Our solution can be used to improve security in a variety of settings, including airports, border crossings, and public events. By enhancing facial recognition capabilities, our solution can help identify individuals of interest and prevent potential security threats. 
Commercial: Our solution can be used in commercial settings, such as parking garages and shopping malls, to monitor vehicle movement and ensure compliance with parking regulations. 

Overall, our proposed solution has the potential to revolutionise the way ANPR and FRS systems are used in a variety of real-world applications, improving accuracy, speed, and cost-effectiveness. By enhancing surveillance capabilities and improving the ability to monitor and track individuals of interest, our solution can enhance public safety and security in a variety of settings.



Citations and References:

Lubna, Mufti, N., & Shah, S. A. A. (2021). Automatic Number Plate Recognition:A Detailed Survey of Relevant Algorithms. Sensors (Basel, Switzerland), 21(9), 3028. https://doi.org/10.3390/s21093028

Hashemi, Nazanin Sadat, Roya Babaei Aghdam, Atieh Sadat Bayat Ghiasi, and Parastoo Fatemi. “Template Matching Advances and Applications in Image Analysis”. American Academic Scientific Research Journal for Engineering, Technology, and Sciences 26, no. 3 (November 20, 2016)
https://asrjetsjournal.org/index.php/American_Scientific_Journal/article/view/2378


Pietrzykowski, Marcin & Sałabun, Wojciech. (2014). Applications of Hidden Markov Model: state-of-the-art. 
https://www.researchgate.net/publication/263775347_Applications_of_Hidden_Markov_Model_state-of-the-art



Nikodem M, Słabicki M, Surmacz T, Mrówka P, Dołęga C. Multi-Camera Vehicle Tracking Using Edge Computing and Low-Power Communication. Sensors. 2020; 20(11):3334. https://doi.org/10.3390/s20113334



Prajapati, G.L. & Patle, Arti. (2010). On Performing Classification Using SVM with Radial Basis and Polynomial Kernel Functions. 512-515. 10.1109/ICETET.2010.134. 
https://www.researchgate.net/publication/261234792_On_Performing_Classification_Using_SVM_with_Radial_Basis_and_Polynomial_Kernel_Functions

Kaur, Parneet & Kumar, Yogesh & Ahmed, Shakeel & Alhumam, Abdulaziz & Singla, Ruchi & Ijaz, Muhammad Fazal. (2021). Automatic License Plate Recognition System for Vehicles Using a CNN. Computers, Materials and Continua. 71. 35-50. 10.32604/cmc.2022.017681.
https://www.researchgate.net/publication/355890014_Automatic_License_Plate_Recognition_System_for_Vehicles_Using_a_CNN
 
