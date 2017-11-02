# ImagePreviewSwift
This is used for preview image.

<b> How to install

POD </b>
<br>You can directly include following in your pod file

    pod 'ImagePreviewSwift', :git => 'https://github.com/RPiyush/ImagePreviewSwift.git', :tag => '0.0.5'
             
<b> How to Use </b>
 
1. Declare Object of class <b>ImageSliderSwift </b> like var myImageSlider: ImageSliderSwift!

2. Add Initialize object function to your file

       func initializeImagePreviewClass(_ imagesArray: [String]) {
         self.myImageSlider = ImageSliderSwift.sharedInstance.initWithParentView(self.view)
         self.myImageSlider.setMarginColor(marginColor: Constants.colors.sliderMarginColor)
         self.myImageSlider.addImagesToView(imagesArray: imagesArray as NSArray)
       }
      
<br> pass colors, which you want to set in Margin, define this in your constant file and pass location in setMarginColor.

       static let sliderMarginColor = UIColor(red: 127.0 / 255.0, green: 127.0 / 255.0, blue: 127.0 / 255.0, alpha: 1.0)

 3. Call Method 'initializeImagePreviewClass' when you have images path Array
 
        self.initializeImagePreviewClass(imagePathArray)
        
 4. Now when image clicked for preview, pass index value of that image. Make sure image location index is same as you passed imagePathArray index.
 
         func imagePreview(_ selectedIndex: Int) {
           self.myImageSlider.setImageIndex(indexValue: selectedIndex)
           self.myImageSlider.showView()
        }


 ## Author
Piyush Rathi, piyush.rathi@kahunasystems.com
