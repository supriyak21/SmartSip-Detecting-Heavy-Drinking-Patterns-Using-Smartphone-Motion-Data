# SmartSip-Detecting-Heavy-Drinking-Patterns-Using-Smartphone-Motion-Data

• Developed a machine learning classifier to detect heavy drinking episodes using smartphone accelerometer data

• Analyzed a dataset of over 30M accelerometer samples from 13 participants in a field study, with transdermal alcohol content (TAC) sensors providing ground truth labels

• Implemented data cleaning and preprocessing techniques:

  Applied 10th order Chebyshev Type II low-pass filter (fstop = 1e-4 Hz) to TAC data
  
  Used 15th order Chebyshev Type II filter (fstop = 2.7 Hz) for accelerometer signals
  
  Segmented data into 10-second windows for analysis
  
• Extracted 1,215 features from accelerometer data, including:

  Time-domain features: mean, standard deviation, zero-crossing rate, etc.
  
  Frequency-domain features: spectral entropy, centroid, flux, roll-off
  
  Gait-related features: step count, cadence, stride length
  
  Novel MFCC covariance matrix features (546 total)
  
• Evaluated multiple machine learning models:

  Random Forest (700 trees)
  
  Support Vector Machine (RBF kernel)
  
  Multilayer Perceptron (256 hidden units)
  
  Convolutional Neural Network
  
• Achieved best performance with Random Forest classifier:

  77.5% overall accuracy
  
  81.5% accuracy for sober state (TAC < 0.08)
  
  69.8% accuracy for intoxicated state (TAC ≥ 0.08)
  
• Demonstrated significant impact of MFCC covariance features:

  Improved Random Forest accuracy by 14.6%
  
  Enhanced SVM accuracy by 11.5%
  
• Analyzed classifier robustness through error analysis, revealing challenges in mid-range TAC detection (0.10-0.15)

• Project outcomes support development of privacy-preserving, real-time interventions for heavy drinking prevention
