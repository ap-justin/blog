this has something to do with aspect ratio

for the cropper, the aspect ratio is set to `4/1`, for the marketplace cards - it's `2/1`
and for the profile banners it's `2.76/1`

<img width="568" alt="image" src="https://user-images.githubusercontent.com/89639563/197445676-4b5d6648-9f35-42ad-a6fe-c3d9a11f2c27.png">

note that the profile banner aspect ratio `2.76/1` is not fixed and changes accordingly to layout. 
> PROFILE TWO-COLUMN VIEW, aspect is around `2.6/1`

<img width="1147" alt="image" src="https://user-images.githubusercontent.com/89639563/197446724-ccb7f66b-aa27-42cb-a354-fc7b0a1392da.png">


> PROFILE SINGLE COLUMN VIEW, aspect is around `3.33/1`

<img width="552" alt="image" src="https://user-images.githubusercontent.com/89639563/197446610-d210468f-d573-4c92-809f-444e28043fc9.png">


NOTE: Having the aspect ratio `fixed` to certain value e.g `3/1` would make it aesthetic on certain layouts but look bad on other
> PROFILE BANNER with `3/1` aspect ratio in desktop view

<img width="1135" alt="image" src="https://user-images.githubusercontent.com/89639563/197446859-85996604-e12f-4ee5-be8b-aa6020d016e2.png">

> PROFILE BANNER with `3/1` ratio in mobile view (banner now is too small)

<img width="561" alt="image" src="https://user-images.githubusercontent.com/89639563/197446951-22ed5790-2bb1-41ea-8f71-c458a3d9c25e.png">

Using the same aspect ratio in marketplace cards, for the sake of being uniform across the app woudn't look good
<img width="333" alt="image" src="https://user-images.githubusercontent.com/89639563/197447684-5b0fc198-a904-48ee-9975-eb7a26173f20.png">




Currently, we set the image to `fill` its container's aspect ratio, leaving out no empty space but crops some part of the image that doesn't fit that aspect ratio

<img width="380" alt="image" src="https://user-images.githubusercontent.com/89639563/197445991-461a8769-abb6-498e-a451-e334686f2dd0.png">


We can set the image to `fit` the container instead, keeping its original aspect ratio but will leave some extra spaces

<img width="633" alt="image" src="https://user-images.githubusercontent.com/89639563/197447187-025aea3d-b6eb-4cf3-9779-0b9ddec3c4c1.png">

Of course we could just make the extra space transparent, but if used e.g in marketplace, would make the cards look uneven
<img width="350" alt="image" src="https://user-images.githubusercontent.com/89639563/197447443-136980f3-128a-408e-8de8-29eea66d464e.png">


In the meantime, we could just set the profile banner and image cropper with the same aspect ratio of `3/1`, but this is not a perfect solution for reasons 
1. if we make profile banner aspect `dynamic`, there would come some screen sizes where the the initial `3/1` would wrap to some other value
2. if we make profile banner aspect `static`, image content is kept, but size would vary to keep that content. This would make banner size inappropriate on some screen sizes
3. the fixed `3/1` isn't guaranteed to look good when used in marketplace cards



