# Phone-Price-Classification-and-Exploratory-Data-Analysis
Exploratory Data Analysis and Machine Learing Classification to Predict Phone Price Range


# Background Information


Personal cellphone has been around since the 1970's, however the first ever smartphone was invented in 1992 by IBM it call [simon personal communicator](https://en.wikipedia.org/wiki/IBM_Simon#Features). 


Then come along the 3G network where it allow a smartphone to be connected to the internet. 


After that in 2007 we have the first iphone where it almost revolutionize the smartphone idustry, as it was the sleekest designed phone and the first smart phone that offered a full unwatered down version of the internet


Fast forward to 2020, since the launch of iphone, major thing that happened to smart phone industry are **The Launch of Android**, the rise of application industry (and the monetazion of them), and more others.

As of today it's [predicted that 2.5 billion people around the worlds own smartphone](https://www.pewresearch.org/global/2019/02/05/smartphone-ownership-is-growing-rapidly-around-the-world-but-not-always-equally/), with the growing numbers of smartphone ownership, the number of smartphone manufacturing is also growing. Smartphone companies launch a product that varies in computational power.


This notebook, is an Exploratory data analysis on smartphone price range and how hardware inside of a smartphone will affect the price of a smartphone.

In this notebook we are going to predict on a smartphone price range based on the hardware feature using a machine learning classification method



# Problem Statement


As the competition of smartphones get more and more competitive each day, finding the best pricing range for a smartphone would be a key strategy to have a profitable smartphone company.

However as there are more and more smartphone it's getting harder and harder for a company to justified a price range of a phone. 

if a company set a smartphone that's too expensive with low computational power nobody is going to buy it, and if a company set a smartphone price range too low based on it's computational power the smartphone company is going to lose on potential profit.


## EDA Goals 


### Findout what specification that affecting phone price range 


- **What are the the specification of a phone that's affecting the price range**
    - Does Screensize matter to the price range
    - Do the camera megapixel affecting the price of a phone
    - How does RAM size affecting the price range

## Machine Learning Goals 

**Predicting Phone Price Range Based on Their Specification**
- **What Machine Learning classification models that has the best evaluation matrix to predict phone price based on their specification**

This prediction could be useful for a mobile phone company to price their phone price range based a specification 


<details>
    <summary><h2> Exploratory Data Analysis (Summary)</h2></summary>
  
 ## EDA Conclusion, Recommendation, and Future Improvement
 
 ### Conclusion

- **What are the specification that affecting phone prices**
 from our analysis using the correlation method and seaborn heatmap, the major specification that affecting the price range are 
       
   1. **RAM Size** the more expensive phone **(higher price range)** has a higher RAM size. From our analysis we found out that the higher the price range the higher the minimum ram size for phones 
        
   2. **Battery Power** for the battery power the min battery power of all phone price range are around 500 mAh, and the maximum battery power of all price range is around 2000 mAh. However the the average battery power keep increasing in general as the price range goes up.and from our analysis the distribution of battery power for phone that's in the higher price range are slight *left skewed* compared to the phone with the lower price range (price range 1 & 0) are slightly *right skewed*
   
   3. **PX height & PX width** pixel height and pixel width are the determinant factor when it comes to screen quality and in this case the height and the width play a role when it comes to determining a price of a phone range, for the pixel width it shows that phone that's in a higher price range has a higher pixel width. however for the pixel width the distribution kind of looks similar for phone in all price range 
   

- **Screen Size and Phone Price Range** 

in general the screen size for phone doesn't really much effect on the price range, the average screen size for phone in **price range 0 - 2** are somewhere around **5.55 inches** to **5.6 inches**. however there's a somewhat of a jump in screensize when it comes to price range 3, the average screensize for price range 3 is somewhere around **5.7 inches**


**HD Screen** For phone that has HD quality screen the screen the trend of screen size kind of similar with the general trend the difference here is that **HD Screen** has a slightly lower screen size in average for price range 0 - 2 compared to the general population, and for the higher price range *(price range 3 )* **HD Screen has a slightly higher average screen size (5.8 Inches)** compared to the entire population.

**Not HD Screen** For non HD phone the screen size of a phone keep getting smaller as the phone price range goes up, the highest average screen size for non HD screen is in price range 0, at around **(5.65)** and the lowest average of screen size is in price range 3 **(5.5)** inches 


- **Camera Megapixel and Price Range**

![image](https://user-images.githubusercontent.com/57277832/97967077-4eb7f500-1def-11eb-8b38-3121d9862467.png)



by looking at the table above we can see that for the **primary camera (back camera)** the average megapixel is somehow positively correlated with the price range , as the average megapixel get higher as  the price range get more expensive.

However for the front camera the size of the megapixel doesn't really have any positive or negative correlation to the price range


## Recommendation 

**RAM Size**

The main factor that's affecting phone price range is **RAM SIZE** so if a phone so if a smartphone company would like to create a phone in a specific price range, the **RAM Size** is one of the specification that needs to be watched carefully, since it's a feature that affecting the price range of a phone from this dataset


Second is **battery power** the more expensive the smartphone the higher the battery sizes it should have, since higher RAM needs more power from the battery, a smartphone company should adjust their battery battery accordingly, and what's all the RAM power if a phone could only last for a couple of hour

**Screen Quality and Screen Size**


Since Pixel width and Pixel Height affecting the HD or Non HD screen quality, this specification needs to be watched before a phone company launch a new product, The Screen size's need to be considered when lauching a new phone, **NON HD** screen should not have **a big screen for phone in price range 3** because of the trend from our analysis, and the image quality will also get pixelated from having too big  of a screen and too low of pixel width and size 


**For HD Screen** as the phone company want to launch a phone in a higher price range, the pixel width and the pixel height of a phone should be in a higher range **(Price Range 3)** as well, and for the screen sizes phone with **HD screen** and high price range, the screen size's should be bigger than the screen size of lower price range


**Camera Megapixel**

From our Analysis it shows that phone with a higher price range has a **higher camera pixel size**, and for the front camera the pixel size of a front phone camera it seems doesn't have a positive or negative correlation with the price range.

so for the phone company **Primary Camera** or back camera megapixel size should be more considerated compared to the front camera

</details>

<details>
    <summary><h2> Machine Learning Summary </h2></summary>
  
  **Conclusion**

- We can see that from all the evaluation matrix for this phone classfication, we see that, **SVC after  hyperparameter tuning without scalling has the best accuracy** when it comes to predicting phone price range based on certain features.

![image](https://user-images.githubusercontent.com/57277832/97968669-8e7fdc00-1df1-11eb-861a-1d02a5928b6d.png)



- We also see that there're some overfitting model, we can see it by looking the the significance difference training score and testing score 

**Recommendation & Improvement**

1. Different features selection for certain models that is overfitting, by looking at the 4 tables above we can clearly see that there's overfitting problem in some of our models, for future references please use a simpler feature selection for overfitted model


2. Reliability of the data, this dataset has a lot of randomness to it, like having **pixel height that's lower than 240px, 0 width for screen and etc**, doing a lot of cleanining replacing random values of the data might have an effect in our model


3. Using Different kind of scaler, in this modeling i use a minmax scaller to scale the X train and X test, fot future references using different kind of scaller might have an effect to the model



</details>
