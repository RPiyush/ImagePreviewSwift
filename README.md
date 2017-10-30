# ImagePreviewSwift
This is used for preview image.

<b> How to install

POD </b>
<br>You can directly include following in your pod file

             pod 'ImagePreviewSwift', :git => 'https://github.com/RPiyush/ImagePreviewSwift.git', :tag => '0.0.4'
             
<b> How to Use </b>
 
1. Declare Object of class <b>ImageSliderSwift </b> like var myImageSlider: ImageSliderSwift!

2. Initialize object 

  func initializePopImageSlider(_ imagesArray: [String]) {
        let height = self.view.bounds.size.height - 200
        let width = self.view.bounds.size.width - 200
        self.myImageSlider = ImageSliderSwift.sharedInstance.initWithFrame(frame: CGRect(x: 0, y: 0, width: width, height: height), parentView: self.view)
        self.myImageSlider.setMarginColor(marginColor: Constants.colors.sliderMarginColor)
        self.myImageSlider.addImagesToView(imagesArray: imagesArray as NSArray)
    }

 ## Author
Piyush Rathi, piyush.rathi@kahunasystems.com
