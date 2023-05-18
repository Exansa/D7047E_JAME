# D7047E_JAME
Exercise and project group in advanced deep learning

## Träning
Jag föreslår att vi jämför transfer learning från enbart ImageNet (ej fruits360) till fruit quality samt från fruits360 (ej ImageNet pre-trained) till fruit quality.

Jag tycker även att vi inte bör använda rotation på quality datasetet eftersom det redan är roterade och translaterade bilder i det.

Markera med en "✓" under det ni kör/kört.
  
På alla:  
Batch size=16, Vertical+Horizontal flip, Rotation=0, Adam
  
ImageNet -> Quality  
Learning rate = 1e-3 &nbsp; |Learning rate = 1e-3  |Learning rate = 1e-4  |Learning rate = 1e-4  
Zoom range = 0    &emsp;  &ensp; |Zoom range = 0.3  &emsp;  &ensp; |Zoom range = 0  &emsp;  &ensp; |Zoom range = 0.3  
  
  
Fruits360 -> Quality  
Learning rate = 1e-3 &nbsp; |Learning rate = 1e-3  |Learning rate = 1e-4  |Learning rate = 1e-4  
Zoom range = 0    &emsp;  &ensp; |Zoom range = 0.3  &emsp;  &ensp; |Zoom range = 0  &emsp;  &ensp; |Zoom range = 0.3  
  
  
VGG-16 (otränat) -> Quality  
Learning rate = 1e-3 &nbsp; |Learning rate = 1e-3  |Learning rate = 1e-4  |Learning rate = 1e-4  
Zoom range = 0    &emsp;  &ensp; |Zoom range = 0.3  &emsp;  &ensp; |Zoom range = 0  &emsp;  &ensp; |Zoom range = 0.3  


Om vi hinner klart dessa så kan vi fortsätta med mer kombinationer.

I filen model_acc_old.txt så ser ni resultat för ImageNet->Fruits360->Quality. Som sagt så föreslår jag att vi inte kör på detta.




### Project
Research om hur andra har gjort - Magnus & Emanuel

Preppa dataset - Arvid & Jacob
- Gör en lista för alla möjliga dataset
- Plocka bort onödiga grönsaker/frukter i Fruits360? (klar)
- Rutten/fräsch (klar)
- Mognadsgrad (abort)
- Proprocess data (vilka transformationer) (typ klar, under testing)

Strukturera upp koden (klar) - Alex & Emanuel

Använd CNNVis

Bestäm evaluation metric: accuracy, recall, precision (klar) 
Fixa transfer learning - Magnus (klar)

Extra features
- Live tracking med kamera - Alex  
- Klassificera flera frukter på samma bild


Strukturera rapport - Emanuel  
Presentation  
Rapport (4-5 sidor article) - Alla


#### Intressanta länkar
Fruit maturity grading framework for small dataset using single image multi-object sampling and Mask R-CNN
https://www.sciencedirect.com/science/article/pii/S2772375522000958

Detection of Overall Fruit Maturity of Local Fruits using Convolutional Neural Networks Through Image Processing
https://dl.acm.org/doi/10.1145/3366650.3366681

Fruit Ripeness Prediction Based on DNN Feature Induction from Sparse Dataset
https://www.techscience.com/cmc/v69n3/44159

#### Dataset 5 maj
https://drive.google.com/file/d/15hFRMZECi5Hi7HA7LVvq86CxbmSRrqCH/view?usp=sharing

#### Transformationer
randomrotation
normalize
RandomPerspective (kanske)
Zoom range
Shear range
Random block (kanske)
