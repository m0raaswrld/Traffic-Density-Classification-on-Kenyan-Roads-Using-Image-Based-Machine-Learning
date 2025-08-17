// ============================================
// Traffic Density Classification – [Mitchelle Moraa]
// ============================================


// ============================================
// 1. Overview
// ============================================
  This project presents a machine learning approach to classify traffic congestion on Kenyan roads using image data. 
  The model distinguishes between **high traffic** and **low traffic** conditions, offering a foundation for 
  AI-driven traffic monitoring and urban planning in developing cities.  

  Objectives:  
  - Collect and preprocess road traffic images from multiple sources  
  - Train a Convolutional Neural Network (CNN) to classify congestion levels  
  - Evaluate model performance using accuracy, ROC AUC, and confusion matrix  
  - Discuss challenges of AI adoption for road safety in Africa  


// ============================================
// 2. Dataset & Preparation
// ============================================
  Sources:  
  - Online image repositories (Bing, Google via icrawler)  
  - Crowdsourced community forums (Reddit, X/Twitter, Telegram)  
  - Local news outlets and NGO archives  

  Cleaning & preprocessing steps:  
  - Resized images to 224×224 pixels  
  - Normalized pixel values (0–1 scaling)  
  - Removed duplicates (ImageHash)  
  - Filtered out blurry/low-quality images (OpenCV Laplacian variance)  
  - Balanced dataset: **119 High Traffic**, **120 Low Traffic**  




// ============================================
// 3. Methodology
// ============================================
  - **Data Collection**: Automated scraping and manual validation  
  - **Preprocessing**: Standardization, balancing, filtering  
  - **Model Training**: CNN architectures (VGG16, ResNet) using PyTorch  
  - **Evaluation**: Accuracy, ROC Curve, Confusion Matrix  




// ============================================
// 4. Key Insights
// ============================================
  - CNN models successfully classified traffic density with promising accuracy (86% baseline).  
  - Clear distinction between peak congestion and free-flow scenarios.  
  - Demonstrates feasibility of **low-cost AI systems** for traffic monitoring in Kenya.  
  - Potential applications in **smart city planning**, **real-time traffic alerts**, and **road safety analysis**.  

  


// ============================================
// 5. Challenges & Solutions
// ============================================
  Challenge: Limited Kenya-specific traffic datasets  
  Solution: Crowdsourced + scraped images, manual balancing  

  Challenge: Image duplication and quality issues  
  Solution: Used ImageHash for duplicate removal, OpenCV for filtering  

  Challenge: Class imbalance (more high-traffic images initially)  
  Solution: Augmentation and sampling to balance dataset  

  Challenge: Limited computing resources  
  Solution: Optimized CNN architectures and used pretrained models  


// ============================================
// 6. Assumptions & Limitations
// ============================================
  - Dataset size is relatively small, may affect generalization  
  - Model trained on static images, not real-time video feeds  
  - Further scaling required for deployment in smart infrastructure  


// ============================================
// 7. Deliverables
// ============================================
  - Dataset: `data/high_traffic/` and `data/low_traffic/`  
  - Notebooks: `notebooks/preprocessing.ipynb`, `notebooks/model_training.ipynb`  
  - Trained Models: `models/traffic_cnn.pth`  
  - Report: `Traffic_AI_Report.pdf`  
  - README.md (this document)  
   
