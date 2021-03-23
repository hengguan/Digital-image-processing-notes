## Histograms and Point Operations

---
- **Histograms plots how many times (frequency) each intensity value in image occurs**

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="./images/01.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">01. histograms example</div>
</center>

**Histograms: only statistical information.**  
**No indication of location of pixels**

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="./images/02.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">02. histograms example</div>
</center>

**Different images can have same histogram.**
- 3 images below have same histogram

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="./images/03.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">03. histograms example</div>
</center>

**Can not reconstruct image from histogram.**

### a histogram for a grayscale image with intensity values in range:

<center>

![4](https://latex.codecogs.com/svg.latex?I(u,v)\in[0,k-1]) 
</center> 

would contain exactly *K* entries  
Each histogram entry is defined as:  
- h(i) = number of pixels with intensity I for all 0 < i < K.  
or 
![4](https://latex.codecogs.com/svg.latex?h(i)=card\left\{(u,v)|I(u,v)=i\right\})  
*card* means that "Number (size of set) of pixels", and "|" is "such that".

**Log scale makes low values more visible**
<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="./images/04.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">04. Interpreting Histograms</div>
</center>

- **contrast range**: Difference between darkest and lightest

Histograms help detect image acquisition issues Problems with image can be identified on histogram:
- Over and under exposure
- Brightness
- Contrast
- Dynamic Range

Point operations can be used to alter histogram. E.g
- Addition
- Multiplication
- Exp and Log
- Intensity Windowing (Contrast Modification)

### Image Brightness
Brightness of a grayscale image is the **average
intensity** of all pixels in image:

<center>

![4](https://latex.codecogs.com/svg.latex?B(I)=\frac{1}{w*h}\sum_{v=1}^{h}\sum_{u=1}^{w}I(u,v))  
</center>

### Image Contrast
The contrast of a grayscale image indicates how easily objects in the image can be distinguished  
**High contrast image**: many distinct intensity values  
**Low contrast**: image uses few intensity values  
<font color=red>Good Contrast</font> is that Widely spread intensity values and large difference between min and max intensity values  
<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="./images/06.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">06. Interpreting Histograms</div>
</center>  
Many different equations for contrast exist  

- example:
<center>

![4](https://latex.codecogs.com/svg.latex?Contrast=\frac{ChangeInLuminance}{AverageLuminance})  
</center>  

- Michalson’s equation for contrast:
<center>

![4](https://latex.codecogs.com/svg.latex?C_M(i)=\frac{max(I)-min(I)}{max(I)+min(I)})  
</center> 
These equations work well for simple images with 2 luminances (i.e. uniform foreground and
background). Does not work well for complex scenes with many luminances or if min and max intensities are small.

---

### Detecting Bad Exposure using Histograms
Exposure? Are intensity values spread <font color=red>(good)</font>( out or bunched up <font color=red>(bad)</font>

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="./images/05.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">05. Interpreting Histograms</div>
</center>


