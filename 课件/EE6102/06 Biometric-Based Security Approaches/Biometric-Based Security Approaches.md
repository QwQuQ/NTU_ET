---
tags:
  - cyber_security
---

# Forms of Authentication

- Proof that you are you because of:
  身份证明方式
	- **Something you have**: token, smart card.
	  **你拥有的东西**：令牌、智能卡。
	- **Something you know**: PIN, password.
	  **你知道的东西**：PIN码、密码。
	- **Something you are**: Biometric.
	  **你是什么**：生物识别。
- For decades, we have relied on passwords to protect information resources. However, the increase in processor speed and improvements in cryptanalysis have made passwords weak protection.
  多年来，我们依赖密码来保护信息资源。然而，随着处理器速度的提高和密码分析技术的进步，密码已成为较弱的保护手段
- What does Biometrics mean?
  什么是生物识别？
	- Comes from the Greek words “Bios: life” and “Metron: to measure”.
	  生物识别来源于希腊词语“Bios：生命”和“Metron：测量”
	- Automated methods of verifying or recognizing the identity of a living person based on physiological or behavioural characteristics.
	  通过基于生理或行为特征的自动化方法来验证或识别一个活体的身份
	- There are two ways of determining if you are you…
	  确定“你是你”的两种方法：
		1. **IDENTIFICATION**
		   **识别**
			- Establishing a person's identity – Who are you?
			  确立一个人的身份 – 你是谁？
			- One to many comparison.
			  一对多比较。
		2. **VERIFICATION**
		   **验证**
			- Involves confirming or denying a person’s claimed identity - Are you who you claim to be?
			  确认或否认某人声称的身份 – 你真的是你声称的那个人吗？
			- One to one comparison
			  一对一比较。
---
- The Biometrics Processes
	- There are two basic biometrics processes: **enrollment** and **authentication**.
![[Pasted image 20250402015225.png#pic_75center|Enrollment]]
![[Pasted image 20250402015243.png#pic_75center|Authentication]]

# Types of Biometric

![[Pasted image 20250402020027.png#pic_75center|]]

- There are two categories of biometric technologies:
  生物识别技术主要分为两类：
- **Physiological**: These mainly consist of fingerprints, the shape of the hand, vein pattern, the eye (iris and retina), and the shape of the face.
  **生理特征**：主要包括指纹、手的形状、静脉纹路、眼睛（虹膜和视网膜）、面部形状。
- **Behavioral**: The most common are voice recognition, signature dynamics (speed of movement of pen, accelerations, pressure exerted etc.), keystroke, voice, gestures, etc.
  **行为特征**：最常见的包括语音识别、签名动态（例如笔的移动速度、加速度、施加的压力等）、按键动作、语音、手势等。

- Physiological are usually considered to offer the benefit of remaining more stable.
  生理特征通常被认为具有更稳定的优势。

# Biometric-Based Authentication

- Biometric-based Authentication refers to the cyber security procedure that involves using biological characteristics of individuals such as retina, iris, voice, facial characteristics, fingerprints etc. to verify people are who they claim to be.
  **基于生物特征的身份认证**是指通过使用个体的生物特征（例如视网膜、虹膜、语音、面部特征、指纹等）来验证人们是否为其声称的身份的网络安全程序。
- This process can be used to control access to physical and digital resources.
  这一过程可以用于控制对物理和数字资源的访问。

## Fingerprint

- It is a biometric technique used to identify and authenticate individuals based on the unique patterns of their fingerprints.
  指纹识别是一种通过指纹独特模式识别和验证个人身份的生物识别技术。
- Fingerprint Anatomy
  指纹结构
	- Ridges and Valleys: Ridges are raised lines on the fingerprint, while Valleys refers to spaces between the ridges.
	  **脊线和谷线**：脊线是指纹上的突起线，而谷线是脊线之间的空间。
	- Minutiae Points: Unique features such as ridge endings and bifurcations (splits in ridges). There are 30 minutia points in fingerprint.
	  **细节点**：独特特征，例如脊线结束点和分叉点（脊线的分裂）。指纹中有30个细节点。
- Fingerprint biometrics measure the pattern and features associated with the friction ridges on fingertips.
  指纹生物识别测量手指上的摩擦脊线相关的模式和特征。
- Fingerprint is the most widely used biometric because it is easy to use, and very inexpensive to deploy.
  指纹是最广泛使用的生物识别技术，因为其使用方便且部署成本低廉。
- Today, there are fingerprint readers built right into popular notebook computers, smart phones and many other devices.
  如今，指纹读取器已经嵌入到流行的笔记本电脑、智能手机及其他许多设备中。
- Fingerprint biometrics work well in either a one-to-one verification or a one-to-many identification application context.
  指纹生物识别在一对一验证或一对多识别应用背景下均表现良好。

### Fingerprint Recognition Workflow

![[Pasted image 20250402020508.png#pic_75center|]]

- Image Acquisition: Fingerprint scanners (e.g., optical, capacitive, ultrasound).
  **图像采集**：指纹扫描仪（例如光学、电容、超声波）。
- Preprocessing
  预处理
	- Image enhancement (e.g., noise reduction, normalization).
	  图像增强（例如降噪、标准化）。
	- Binarization: Convert grayscale images to binary.
	  二值化：将灰度图像转换为二值图像。
	- Thinning: Reduce ridge thickness to a single pixel width.
	  细化：将脊线厚度减少到单像素宽度。
- Feature Extraction
  特征提取
	- Detect minutiae points and ridge flow.
	  检测细节点和脊线流向
	- Analyze singular points (e.g., core and delta points).
	  分析独特点（例如核心点和三角点）。
- Matching
  匹配
	- Compare extracted features with stored templates using algorithms like ridge correlation, minutiae-based matching, or pattern-based matching.
	  使用算法（例如脊线相关、基于细节点匹配或基于模式匹配）比较提取的特征与存储模板。
- Decision
  决策
	- Authentication or identification based on match score and threshold.
	  根据匹配分数和阈值进行认证或识别。

### Key Algorithms and Challenges in Fingerprint

- Minutiae-Based Matching
  基于细节点匹配
	- Compares minutiae points between two fingerprints. Most widely used but sensitive to image quality.
	  比较两个指纹间的细节点。虽然广泛使用，但对图像质量敏感。
- Correlation-Based Matching
  基于相关性匹配
	- Measures similarity by aligning ridges. Computationally intensive.
	  通过对齐脊线测量相似性。计算密集程度。
- Deep Learning Models
	- Use convolutional neural networks (CNNs) for feature extraction and matching. Robust to noise and distortion.
	  使用卷积神经网络（CNN）进行特征提取和匹配，对噪声和失真具有健壮性。
---
- Challenges in Fingerprint Recognition
	- **Quality of Fingerprint Images**: Factors like dirt, cuts, or worn ridges can degrade quality.
	  **指纹图像质量**：如污垢、割伤或磨损的脊线会降低图像质量。
	- **Spoofing and Security**: Fake fingerprints using materials like gelatin can trick systems.
	  **欺骗和安全问题**：使用明胶等材料制作的假指纹可能欺骗系统。
	- **Variability**: Intraclass variations due to pressure, orientation, or environmental conditions.
	  **变异性**：压力、方向或环境条件导致的同类变异。

### Summary

- ADVANTAGES
	- Low cost and fast
	- Ease of integration and easy to use
	- Non-invasive.
- DISADVANTAGES
	- Fingerprint is easier to steal (is left on everything we touch)
	- High quality copies of fingerprints can be made by using different techniques
	- Environment and usage can affect measurements
	- Cannot be reset once compromised
	  一旦泄漏无法重置
	- Requires good-quality images for optimal performance.
- FUTURE TRENDS
	- Multimodal Biometrics: Combining fingerprints with other biometrics like facial or iris recognition.
	  多模态生物识别：结合指纹与其他生物识别技术（如面部或虹膜识别）
	- AI and Machine Learning: Enhancing feature extraction and spoof detection.
	  人工智能和机器学习：增强特征提取和欺骗检测

## Iris

- Iris is an exciting biometric technology that measures the patterns of the iris which is the coloured area around the pupil of the eye.
  虹膜是一种令人兴奋的生物识别技术，通过测量眼睛瞳孔周围彩色区域的虹膜图案来实现。
- Because there is significantly more information that can be measured, iris is considered the most accurate biometric.
  由于可以测量的信息显著更多，虹膜被认为是最准确的生物识别技术。
- Iris recognition can be accomplished from a distance of one to three feet and uses a light source about as intense as the one on your television remote control.
  虹膜识别可以在一到三英尺的距离内完成，并使用类似于电视遥控器光源强度的光源。
- Iris is growing in popularity in the healthcare sector to protect access to patient electronic records.
  虹膜识别在医疗保健领域的应用日益增长，用于保护患者电子记录的访问权限。
- The concept of Iris Recognition was proposed by Dr. Frank Burch in 1939.
  虹膜识别的概念由Dr. Frank Burch于1939年提出。
- It was first implemented in 1990 when Dr. John Daugman created the algorithms for it.
  该技术首次于1990年实现，当时Dr. John Daugman为其创建了算法。

### Iris Recognization Workflow

- Image Acquisition
  图像采集
	- Capturing a high-quality image of the iris using specialized cameras.
	  使用专业摄像机捕捉高质量的虹膜图像
	- Often performed under near-infrared (NIR) light to enhance pattern visibility and reduce interference from eye color.
	  通常在近红外（NIR）光下进行，以增强图案的可见性并减少眼睛颜色的干扰
- Preprocessing
  预处理
	- Segmentation: Detect the iris region by isolating it from the sclera (white part), pupil, and eyelids.
	  分割：通过将虹膜与巩膜（白色部分）、瞳孔和眼睑分离来检测虹膜区域
	- Normalization: Transform the circular iris into a rectangular block for consistent analysis (rubber-sheet model).
	  归一化：将圆形虹膜转化为矩形块，以便于一致分析（橡皮片模型）
	- Image Enhancement: Improve contrast and reduce noise for better pattern visibility.
	  图像增强：提高对比度并减少噪声以增强图案的可见性
- Feature Extraction
  特征提取
	- Identify and encode unique patterns in the iris.
	  识别并编码虹膜中的独特图案
	- Algorithms analyze texture, frequency, and spatial details.
	  算法分析纹理、频率和空间细节

### Iris Matching

- Matching
	- Compare the encoded template with stored templates in the database.
	  将编码模板与数据库中的存储模板进行比较
	- Algorithms calculate a similarity score based on Hamming distance or correlation.
	  算法根据汉明距离或相关性计算相似度得分
- Decision
	- Authentication or identification based on a threshold value for matching.
	  根据匹配的阈值进行认证或识别
- Key Algorithms in Iris Recognition
	- Daugman’s Algorithm
		- Uses Gabor wavelets to encode and match iris patterns.
		  使用Gabor小波对虹膜图案进行编码和匹配
		- Most widely adopted method in commercial systems.
		  是商业系统中最广泛采用的方法
	- Wavelet-Based Techniques
		- Analyze frequency and orientation of patterns.
		  分析图案的频率和方向性
	- Deep Learning Models
		- CNNs and neural networks for robust feature extraction and matching, especially in challenging conditions.
		  使用卷积神经网络（CNNs）和神经网络进行稳健的特征提取和匹配，特别是在复杂条件下

### Iris Recognition Diagram

![[Pasted image 20250402021851.png#pic_75center|]]

### Summary

- ADVANTAGES
	- High Accuracy: Very low false acceptance and rejection rates.
	  高精度：误接受率和误拒绝率非常低
	- Non-Intrusive: Captured from a distance without physical contact.
	  非侵入性：可以从远处捕获图像，无需身体接触
	- Unique and Stable: Patterns are distinct and do not change over time.
	  独特且稳定：图案独特，且不会随时间改变
- DISADVANTAGES
	- Not easy to use.
	  不易使用
	- System integration is complicated.
	  系统集成较为复杂
	- Cost is also an issue, particularly for high quality iris-based system.
	  成本较高，尤其是高质量的虹膜识别系统
	- Image Acquisition: Poor lighting, motion blur, or occlusions (e.g., eyelashes, eyelids, reflections) can affect quality.
	  图像采集：光线不足、运动模糊或遮挡（如睫毛、眼睑、反射）会影响质量
	- Spoofing Risks: High-resolution printed images or contact lenses can sometimes deceive systems.
	  欺骗风险：高分辨率的打印图像或隐形眼镜有时可以欺骗系统
	- Scalability: Matching in large databases requires efficient algorithms.
	  可扩展性：在大型数据库中进行匹配需要高效的算法
	- Environment Dependence: Outdoor or variable lighting conditions can pose challenges.
	  环境依赖性：室外或可变光照条件可能带来挑战

## Retinal

- Retina scanning is based on the unique patterns of blood vessels in the retina, located at the back of the eye.
  视网膜扫描基于视网膜中血管的独特模式，视网膜位于眼睛后部
- It is one of the most secure and accurate biometric techniques but is not considered a mainstream biometric because it requires proximity to the lens and shines a light source into the eye.
  它是最安全和最准确的生物识别技术之一，但因需要靠近镜头并向眼睛发射光源而未被视为主流生物识别技术
- How it works
	- Image Capture: The retina scanner directs a low-intensity infrared light into the eye. The light illuminates the blood vessels in the retina, which absorb more light than surrounding tissues, making them stand out.
	  图像捕获：视网膜扫描仪向眼睛发射低强度红外光。这种光照亮视网膜中的血管，血管比周围组织吸收更多光线，从而显得突出
	- Pattern Extraction: The scanner captures a digital image of the retina’s blood vessel patterns.
	  图案提取：扫描仪捕获视网膜血管图案的数字图像
	- Feature Analysis: The unique vascular patterns are analyzed and encoded into a biometric template.
	  特征分析：分析并编码独特的血管模式为生物识别模板
	- Matching: The captured retina data is compared with stored templates in a database for verification or identification.
	  匹配：将捕获的视网膜数据与数据库中的存储模板进行比较以验证或识别身份

### Summary

- AVANTAGES
	- High Accuracy: Extremely low false acceptance and rejection rates.
	  高精度：误接受率和误拒绝率极低
	- Security: Difficult to spoof due to the complexity of retinal patterns.
	  安全性：由于视网膜图案的复杂性，难以欺骗
	- Non-Replicable: Patterns are internal to the eye, making them nearly impossible to replicate.
	  不可复制：图案位于眼睛内部，几乎无法复制
- DISADVANTAGES
	- User Cooperation: Requires the individual to remain still and focus on a specific point for a few seconds.
	  用户配合：需要用户保持静止并集中注意力在特定点几秒钟
	- Equipment Costs: Retina scanners are expensive and require specialized hardware.
	  设备成本：视网膜扫描仪昂贵且需要专用硬件
	- Health Concerns: Some users may feel discomfort due to the proximity of the scanner to the eye.
	  健康问题：由于扫描仪与眼睛的距离过近，有些用户可能会感到不适
	- Environmental Sensitivity: Lighting conditions or user movement can affect scan quality.
	  环境敏感性：光照条件或用户运动可能影响扫描质量
	- Does not perform well where user wears spectacles or has cataracts.
	  对佩戴眼镜或患有白内障的用户表现不佳

## Face Recognition

- The human face provides features and measurements of distance and angle that can be computed in two or three dimensions to determine a person’s identity.
- While not as accurate as fingerprint technology, face recognition has significant benefits as an automated verification and identification tool.
- For one it uses a familiar digital photo process that most people are accustomed to and comfortable with.
- Face recognition can be performed from a distance without requiring the user to touch the device.
- Based upon the Distance between the eyes, Width of the nose, Depth of the eye sockets, Shape of the cheekbones, Length of the jawline, etc.
- Holistic facial recognition analyzes a subject’s whole face to find identifying features that match the target.
- Feature-based facial recognition separates the relevant recognition data from the face, then applies it to a template that’s compared against potential matches.

### Face Recognition Workflow

- Image Acquisition: Capture a facial image using cameras (2D or 3D).
  图像采集：使用摄像头（2D或3D）捕捉面部图像
- Preprocessing: Identify and isolate the face in the image using algorithms like Haar cascades, HOG (Histogram of Oriented Gradients), or deep learningbased detectors (e.g., MTCNN).
  预处理：使用算法（如Haar级联分类器、方向梯度直方图（HOG）或基于深度学习的检测器（如MTCNN））识别并分离图像中的面部
- Feature Extraction: Extract unique features like distance between eyes, nose shape, and jawline using techniques such as:
  特征提取：提取独特特征，如眼睛之间的距离、鼻子的形状和下颌线，使用以下技术
	- Eigenfaces (PCA): Statistical analysis of facial features.
	  Eigenfaces（PCA）：对面部特征进行统计分析
	- Local Binary Patterns (LBP): Texture-based features.
	  局部二值模式（LBP）：基于纹理的特征
	- Deep Learning Models: CNNs to extract high-dimensional, robust features (e.g., FaceNet, VGGFace).
	  深度学习模型：使用卷积神经网络（CNNs）提取高维鲁棒特征（如FaceNet、VGGFace）
- Matching
	- Compare the extracted features with stored templates in a database using similarity metrics like cosine similarity or Euclidean distance.
	  使用相似度度量（如余弦相似度或欧几里得距离）将提取的特征与数据库中的存储模板进行比较
- Decision
	- Determine identity or verify authenticity based on a similarity.
	  根据相似性确定身份或验证真实性

### Key Algorithms in Face Recognition

- Face recognition has evolved significantly over the years, and various algorithms are used to enhance accuracy and robustness. Below are the major algorithms in face recognition.
  面部识别技术多年来取得了显著进步，为了提高精确度和鲁棒性，使用了多种算法。以下是面部识别中的主要算法
- Principal Component Analysis (PCA)
  主成分分析 (PCA)
	- Is a dimensionality reduction technique that identifies patterns in facial data by projecting images onto a lower-dimensional space (called Eigenfaces).
	  一种降维技术，通过将图像投影到低维空间（称为特征脸）来识别面部数据中的模式
	- Key Features
		- Captures global variations in the face.
		  捕捉面部的全局变化
		- Computationally efficient for small datasets.
		  对小型数据集计算效率高
	- Limitations
		- Sensitive to lighting, pose, and expression variations.
		  对光照、姿势和表情变化敏感
		- Less effective for large-scale and real-time systems.
		  对大规模和实时系统效果较差
- Linear Discriminant Analysis (LDA)
  线性判别分析
	- LDA focuses on maximizing the separability between different classes (identities) by finding linear combinations of features.
	  LDA 通过寻找特征的线性组合来最大化不同类别（身份）之间的可分性
	- Key Features
		- Reduces within-class variance and increases between-class variance.
		  减少类内方差，增加类间方差
		- Works better than PCA for multi-class face recognition problems.
		  对多类别面部识别问题比 PCA 效果更好
	- Limitations
		- Computationally expensive for high-dimensional data.
		  对高维数据计算成本高
		- Requires large, labeled datasets for effective training.
		  需要大型标注数据集以实现有效训练
	- Local Binary Patterns (LBP)
	  局部二值模式 (LBP)
		- LBP is a texture-based algorithm that divides a face into regions and extracts local texture features for comparison.
		  一种基于纹理的算法，将面部分成多个区域并提取局部纹理特征进行比较
		- Key Features
			- Robust to lighting variations. Works well in real-time systems due to low computational cost.
			  对光照变化具有鲁棒性。由于计算成本低，适用于实时系统
		- Limitations
			- Sensitive to pose and expression changes. Captures local features only, ignoring global face structure.
			  对姿势和表情变化敏感。仅捕捉局部特征，忽略面部整体结构
	- Histogram of Oriented Gradients (HOG)
	  梯度方向直方图 (HOG)
		- HOG is an image descriptor that captures edge and gradient structure information. Often used for face detection and feature extraction.
		  HOG 是一种图像描述符，用于捕捉边缘和梯度结构信息。常用于面部检测和特征提取
		- Key Features
			- Effective for detecting faces in cluttered backgrounds. Works in conjunction with classifiers like Support Vector Machines (SVMs).
			  在复杂背景中检测面部效果好。通常与支持向量机（SVM）等分类器配合使用
		- Limitations
			- Does not inherently handle pose and scale variations. Not as accurate as deep learning methods.
			  本质上无法处理姿势和尺度变化。精确度不如深度学习方法
	- Convolutional Neural Networks (CNNs)
	  卷积神经网络 (CNNs)
		- CNNs are used to extract hierarchical features (e.g., edges, shapes, and textures) from facial images.
		  CNNs 用于从面部图像中提取分层特征（如边缘、形状和纹理）
		- Examples: AlexNet, VGGFace, ResNet.
		- Strengths: Handles pose, lighting, and expression variations well. Highly accurate with large datasets
		  能很好地处理姿势、光照和表情变化。对大型数据集具有高精度
	- Deep Metric Learning (e.g., FaceNet, ArcFace)
	  深度度量学习 (例如 FaceNet、ArcFace)
		- These methods learn a mapping from face images to a feature space where faces of the same person are close together, and different individuals are far apart.
		  这些方法学习将面部图像映射到特征空间，在该空间中同一人的面部特征彼此接近，而不同个体的特征彼此远离
		- FaceNet uses a triplet loss function to optimize embeddings while ArcFace employs angular margin loss for improved discrimination.
		  FaceNet 使用三元组损失函数优化嵌入，而 ArcFace 使用角度边距损失以提高辨别能力
	- Fisher faces Description
		- Combines PCA and LDA to create a robust algorithm
		  结合 PCA 和 LDA 创造出一种鲁棒的算法
		- Effective in handling variations like illumination and expression.
		  能有效处理光照和表情变化等情况
		- Less effective with large datasets.
		  对于大型数据集效果较差
	- Elastic Bunch Graph Matching (EBGM)
	  弹性束图匹配 (EBGM)
		- Models the face using Gabor wavelet features to construct a graph. Matching is performed based on the similarities between graph nodes.
		  使用 Gabor 小波特征构建图形来建模面部。基于图节点之间的相似性进行匹配
		- Robust to moderate pose variations.
		  对中等姿势变化具有鲁棒性
		- Computationally intensive.
		  计算密集型

## 3D Face Recognition

- The 3D facial recognition method involves using sensors to capture the shape of the face with more precision.
  3D面部识别方法使用传感器捕捉面部的形状，更加精确
- Unlike traditional facial recognition methods, the accuracy of 3D facial recognition is not affected by lighting, and scans can even be done in the dark.
  与传统面部识别方法不同，3D面部识别的精确度不受光线影响，甚至可以在黑暗中扫描
- Another advantage of 3D facial recognition is that it can recognize a target from multiple angles.
  3D面部识别的另一个优点是可以从多个角度识别目标
- The 3D facial recognition process has below main steps.
	1. Detection: Face can be captured directly as a 3D image by facial recognition cameras, or it can be captured by scanning a 2D photo.
	   检测：通过面部识别摄像头直接捕捉3D图像，或通过扫描2D照片捕捉
	2. Alignment: The face recognition Algorithm determines the position and angle of the face, as well as its size.
	   对齐：面部识别算法确定面部的位置、角度及大小
		- As long as the face is oriented within 90 degrees of facing the camera, 3D facial recognition software can identify it.
		  只要面部朝向摄像头的角度在90度以内，3D面部识别软件即可识别
	3. Measurement: Once the image has been detected, the system measures (down to the sub-millimeter) the shape of the face. Once it has achieved this very accurate measurement, a template is created.
	   测量：图像被检测到后，系统以亚毫米级精度测量面部形状。一旦完成精确测量，就会创建一个模板
	4. Matching: The matching step involves searching the database to find a match for the newly converted template. If the database being searched is made up entirely of 3D images, a match can be made without any extra steps.
	   匹配：匹配步骤包括在数据库中搜索新转换的模板是否匹配。如果数据库完全由3D图像组成，可直接匹配，无需额外步骤
		- If the database also has 2D images, the software uses an algorithm to convert the 3D facial image into 2D to find a match.
		  如果数据库中还有2D图像，软件会使用算法将3D面部图像转换为2D以找到匹配项
	5. Verification or identification: Depending on the situation, the 3D facial recognition software can either verify or identify the face.
	   验证或识别：根据情况，3D面部识别软件可以验证或识别面部
		- Verification is used to confirm the identity.
		  验证用于确认身份
---
- The accuracy of facial recognition technology has improved over the past few years. In 2014, the top-performing algorithm had an error rate of 4.1%; while currently, the best algorithm reported a mere 0.08% error rate.
  面部识别技术的准确性在过去几年中有了很大提升。2014年，表现最佳的算法错误率为4.1%；而目前，最佳算法仅报告了0.08%的错误率
- If the image analyzed is perfectly clear, the subject can be identified with up to 99.97% accuracy. However, in the real world, photos are often taken in lessthan-ideal conditions (poor lighting, awkward facial profiles, and so on), and false face recognition matches can easily happen.
  如果所分析的图像非常清晰，最多可达99.97%的准确识别率。然而，在现实中，照片通常是在不理想的条件下拍摄的（如光线不足、面部角度尴尬等），因此很容易出现错误匹配
- Researchers are developing Skin Texture and face recognition which can significantly increase the accuracy of face recognition technology
  研究人员正在开发皮肤纹理与面部识别技术，这可以显著提高面部识别技术的准确性

# Biometric Authentication System Challenges

![[Pasted image 20250402024731.png#pic_75center|]]

## Biometrics Error Rates

![[Pasted image 20250402024855.png#pic_50center|]]

- Each biometrics solution has three associated error rates:
  每种生物识别解决方案都有三个相关的错误率
	1. False rejection rates (FRRs), known as Type I errors, are the rate at which an authentication system fails to verify the identity of an authorized user.
	   拒绝率（FRR），称为I型错误，指认证系统未能验证授权用户身份的频率
	2. A Type II error, the false acceptance rate (FAR), is the rate at which the authentication system incorrectly authenticates unauthorized users.
	   II型错误，即假接受率（FAR），指认证系统错误地验证未经授权用户身份的频率
	3. The crossover error rate, or CER, is the point at which the FAR and the FRR are the same.
	   交叉错误率（CER），是FAR和FRR相等的点
- As we increase the sensitivity of the biometrics sensors, the FRR increases, and the FAR decreases.
  随着生物识别传感器敏感度的提高，FRR增加，FAR减少
- In other words, as we try harder to prevent unauthorized users from getting authenticated, we frustrate genuine users, as we increase the number of times an authorized user fails to authenticate.
  换句话说，当我们努力防止未经授权的用户被认证时，我们可能会让真正的用户感到沮丧，因为授权用户失败认证的次数增加了。
- When selecting a solution, it is crucial to understand the risk associated with the error rates and choose the one that fits the specific application within your organization.
  在选择解决方案时，了解与错误率相关的风险并选择适合组织具体应用的解决方案至关重要。

## Biometric Errors and Deception

- ERRORS: when subject is not trying to fool the system
  错误：当对象没有试图欺骗系统时出现的错误。
- DECEPTION: when subject is trying to fool the system
  欺骗：当对象试图欺骗系统时出现的情况
- Vendor Claims for FARs and FRRs
  供应商对假接受率（FAR）和假拒绝率（FRR）的主张
	- Tend to be exaggerated through tests under ideal conditions
	  往往通过理想条件下的测试进行夸大
- Failure to Enroll (FTE)
	- Subject cannot enroll in system
	  对象无法在系统中注册
	- E.g., poor fingerprints due to construction work, clerical work, age, etc.)
	  例如，因建筑工作、文职工作、年龄等导致指纹质量差
- Other Factors Affecting Performance
	- Demographics (youth, aged, ethnic origin, gender, occupation).
	  人口统计（青年、老年、种族来源、性别、职业）
	- Template Age.
	  模板年龄
	- Physiology (hair, disability, illness, injury, height, features, time of day).
	  生理状况（头发、残疾、疾病、受伤、身高、特征、一天中的时间）
	- Appearance (clothing, cosmetics, tattoos, adornments, hair-style, glasses, contact lenses, bandages).
	  外观（服饰、化妆品、纹身、装饰品、发型、眼镜、隐形眼镜、绷带）
	- Behavior (language, accent, pose, positioning, nervousness, distractions).
	  行为（语言、口音、姿势、定位、紧张、分心）

# How Biometric System is Attacked

- Presentation Attacks: Use an artifact, something used to mimic the relevant biometric of a user, to authenticate as an enrolled user.
  呈现攻击：使用伪造物品模仿用户的相关生物特征，以认证为已注册用户身份
- Sensor Output Interception: Capture reference templates and use them during an attack.
  传感器输出拦截：捕获参考模板并在攻击中使用
- Reference and Database: Vulnerabilities enable unauthorized access to reference templates which attacker can misuse for attacks.
  参考和数据库：漏洞使未经授权的访问参考模板成为可能，攻击者可以利用这些模板进行攻击
- The integrity of the Enrollment: It is compromised when a threat actor can enroll for an authorized user with a scan of the threat actor instead.
  注册的完整性：当威胁行为者使用自己的扫描数据来注册为授权用户时，完整性会受到损害
- Insider Threats: Attacker can work alone or in collaboration with outside threat actors to steal/misuse biometric templates and launches cyber attacks.
  内部威胁：攻击者可以单独行动或与外部威胁行为者协作窃取或滥用生物识别模板并发动网络攻击
- Of course, not all biometrics solutions are susceptible to all these above attacks.
  当然，并不是所有生物识别解决方案都容易受到上述攻击的影响
- The key takeaway, however, is that biometrics is not a completely safe authentication factor.
  关键点在于，生物识别并不是一种完全安全的身份验证方式
- It has cyber security risk associated with it such as the quality of the sensors, and the processing algorithms and overall security in place.
  它存在网络安全风险，例如传感器质量、处理算法及现有的整体安全措施

# Summary

- Advantages
	- Difficult to Hack: Biometric systems are incredibly difficult to hack as it can’t be guessed or cracked like passwords.
	  难以破解：生物识别系统非常难以被破解，因为它不像密码那样可以被猜测或破解
	- Convenient: Biometric scans are a lot faster than typing in a password. Biometric also eliminates the need to remember multiple strong passwords and the frustration of constantly forgetting them.
	  方便快捷：生物识别扫描比输入密码快得多。生物识别还消除了记忆多个复杂密码以及不断忘记密码的烦恼
	- Always Available: You can easily forget your phone or keycard, at home, but it’s unlikely you'll forget your fingers or face. Biometric scanners let you log-in wherever you are, without the need for additional authentication devices.
	  随时可用：你可能会忘记手机或门禁卡，但不太可能忘记自己的手指或面部。生物识别扫描仪允许你随时随地登录，无需额外的认证设备
- Disadvantages
	- Complacency: Biometrics on smartphones are so convenient that they can easily become second nature. This can lead to recklessness when logging in. A biometric is only as safe as the person scanning it.
	  自满心理：智能手机上的生物识别功能如此便捷，以至于可能成为一种习惯。这可能在登录时导致鲁莽行为。生物识别的安全性取决于使用者的操作方式
	- High risk: You can change passwords, but you can’t change your biometric details. If your biometric data is stolen or lost, it could be permanently compromised.
	  高风险：密码可以更改，但生物识别信息无法更改。如果生物识别数据被盗或丢失，可能会永久受损
	- Duplication/Cloning: Biometric credentials are easier to obtain and duplicate than access cards or keys, because we quite literally leave our biometric footprints and fingerprints everywhere we go.
	  复制/克隆：生物识别凭证比门禁卡或钥匙更容易获取和复制，因为我们的生物信息会留在我们到过的地方
	- Fingerprints can be lifted from physical items such as your keyboard or even recreated from a high-definition photograph. Facial recognition scanners can be tricked by models built from photos on Facebook and other social media sites.
	  指纹可以从物体表面（如键盘）提取，甚至可通过高分辨率照片重现。面部识别扫描仪可能被通过社交媒体照片制作的模型欺骗

## Conclusion

- Biometrics provide convenience and an additional layer of security but are not foolproof.
  生物识别技术提供了便利性和额外的安全层，但并非万无一失
- Their immutability, potential for misuse, and susceptibility to spoofing mean they are best used alongside, not in place of, passwords in most scenarios.
  由于其不可变性、潜在的滥用风险以及易受欺骗的特性，在大多数情况下，生物识别技术最好与密码一起使用，而不是完全取代密码
- Biometrics can enhance, but not replace, passwords.
  生物识别技术可以增强密码的安全性，但不能替代密码