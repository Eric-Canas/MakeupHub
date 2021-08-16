# MakeupHub

Draw a beautiful makeup on your face and share it with others.

Makeup-Hub allows you to paint and put some stickers your face, and see how it looks in you or your friends faces from any perspective. In a close future it will also allow you to upload this makeup to a cloud where you could also try how other users makeups looks in your face. Additionally it have an option for <i>moonifying</i> your face, which is really to see how it looks in a plain perspective that is used internally, but is pretty funny :full_moon_with_face:. Everything runs on frontend, so no images are sent to the server.

### Quick Start

Simply run the <a href="./src/public/play.html" target="_blank">./src/public/play.html</a> in server mode.

Turn on your **webcam** click on **Makeup!** and draw a beatiful artwork on your face.  
<img alt="Make up" title="Make up" src="./documentation/exampleImages/Drawing.gif" width=400>

Then see how does it fits you, or try to <i>moonify</i> your face :full_moon_with_face:.  
<img alt="Make up" title="Make up" src="./documentation/exampleImages/Moonifying.gif" width=400>

Or try to **Copy-Paste** some shitty images on your cheeks, a face mask or whatever you want (drawing or pasting images over your <i>moonified</i> face will adjust them better to your skin).  

<img alt="Shitty Stickers" title="Shitty Stickers" src="./documentation/exampleImages/ShittyStickers.gif" width=400 align=left>
<img alt="Face Mask" title="Face Mask" src="./documentation/exampleImages/FaceMask.gif" width=400>


## Implementation Details

This web application is built with <a href=https://www.tensorflow.org/js target="_blank"><img alt="TensorFlow.js" title="TensorFlow.js" src="https://img.shields.io/static/v1?label=&message=Tensorflow.js&color=FF6000&logo=TensorFlow&logoColor=FFFFFF" height=18></a> and
<a href=https://github.com/Eric-Canas/Homography.js target="_blank"><img alt="Homography.js" title="Homography.js" src="https://img.shields.io/static/v1?label=&message=Homography.js&color=8a8a88&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTA4MCIgaGVpZ2h0PSIxMDgwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxkZWZzPjxmaWx0ZXIgaWQ9ImQiIHg9IjAiIHk9IjAiIHdpZHRoPSIxIiBoZWlnaHQ9IjEiIGNvbG9yLWludGVycG9sYXRpb24tZmlsdGVycz0ic1JHQiI+PGZlR2F1c3NpYW5CbHVyIHN0ZERldmlhdGlvbj0iLjQiLz48L2ZpbHRlcj48ZmlsdGVyIGlkPSJjIiB4PSItLjEiIHk9Ii0uMiIgd2lkdGg9IjEuMiIgaGVpZ2h0PSIxLjMiIGNvbG9yLWludGVycG9sYXRpb24tZmlsdGVycz0ic1JHQiI+PGZlR2F1c3NpYW5CbHVyIHN0ZERldmlhdGlvbj0iMy44Ii8+PC9maWx0ZXI+PGZpbHRlciBpZD0iYiIgeD0iMCIgeT0iMCIgd2lkdGg9IjEiIGhlaWdodD0iMSIgY29sb3ItaW50ZXJwb2xhdGlvbi1maWx0ZXJzPSJzUkdCIj48ZmVHYXVzc2lhbkJsdXIgc3RkRGV2aWF0aW9uPSIuMiIvPjwvZmlsdGVyPjxmaWx0ZXIgaWQ9ImEiIHg9IjAiIHk9IjAiIHdpZHRoPSIxIiBoZWlnaHQ9IjEiIGNvbG9yLWludGVycG9sYXRpb24tZmlsdGVycz0ic1JHQiI+PGZlR2F1c3NpYW5CbHVyIHN0ZERldmlhdGlvbj0iLjIiLz48L2ZpbHRlcj48L2RlZnM+PHBhdGggdHJhbnNmb3JtPSJtYXRyaXgoMi44NTM0IDAgMCAyLjgzOTUgLTkxMCAtODY2KSIgZD0iTTMyMyA1NTRWMzgybDYwLTMxIDYwLTMyIDIwIDEyIDE5IDExLTE5IDEwLTU5IDMwLTQyIDIydjExNWwxMDYgNTggMSAydjM4YTYwNjQgNjA2NCAwIDAxLTEwNy01NyA4NjMgODYzIDAgMDAxIDgybC00MSAyOCAxLTExNnoiIGZpbGw9IiMzMzMiIGZpbHRlcj0idXJsKCNhKSIvPjxwYXRoIHRyYW5zZm9ybT0ibWF0cml4KDIuODUzNCAwIDAgMi44Mzk1IC05MTAgLTg2NikiIGQ9Ik02NzUgNjU3bC0yMC0xNCAxLTQxdi00MWExNTkzIDE1OTMgMCAwMC0xMDcgNTd2LTIwbDEtMjAgNTItMjkgNTQtMjkgMS01OHYtNTZsLTItMmE0MjQzIDQyNDMgMCAwMC0xMTctNjJsMzctMjIgNjAgMzEgNjAgMzJ2MThsMSAyNzAtMjEtMTR6IiBmaWxsPSIjMzMzIiBmaWx0ZXI9InVybCgjYikiLz48cGF0aCBkPSJNNDg1IDkxN2wtNTYtMzAtMS0yNC0xLTU3di0zNGw1NyAzMSA1OSAzMSA1OC0zMCA1Ny0zMCAxIDU2djU2bC01NyAzMS01OCAzMS01OS0zMXoiIGZpbGw9IiNmZDUiLz48cGF0aCB0cmFuc2Zvcm09Im1hdHJpeCgyLjg1MzQgMCAwIDIuODM5NSAtOTEwIC04NjYpIiBkPSJNNDk4IDYzMmwtMTktMTAtOS01di00bC0xLTIwdi0xNmw1IDNjMzMgMTggMzUgMTkgMzcgMThsMTItNiAxOS0xMCA4LTR2MzlsLTIwIDExLTIwIDEwLTEyLTZ6IiBmaWxsPSIjZDQ4MDAwIiBmaWx0ZXI9InVybCgjYykiIG9wYWNpdHk9Ii44Ii8+PHRleHQgdHJhbnNmb3JtPSJtYXRyaXgoMi45NzYxIDAgMCAzLjA2MzQgLTgzOSAtMTAzMSkiIHg9IjQwMyIgeT0iNTI3LjQiIGZpbGw9IiMxNzE3MTciIGZpbHRlcj0idXJsKCNkKSIgZm9udC1mYW1pbHk9IkR1YmFpIiBmb250LXNpemU9IjEzMi4xIiBmb250LXdlaWdodD0iNTAwIiBsZXR0ZXItc3BhY2luZz0iMCIgb3BhY2l0eT0iLjkiIHN0cm9rZS13aWR0aD0iLjciIHN0eWxlPSJmb250LXZhcmlhbnQtY2Fwczpub3JtYWw7Zm9udC12YXJpYW50LWVhc3QtYXNpYW46bm9ybWFsO2ZvbnQtdmFyaWFudC1saWdhdHVyZXM6bm9ybWFsO2ZvbnQtdmFyaWFudC1udW1lcmljOm5vcm1hbDtsaW5lLWhlaWdodDoxLjI1O21peC1ibGVuZC1tb2RlOm5vcm1hbCI+PHRzcGFuIHg9IjQwMyIgeT0iNTI3LjQiIG9wYWNpdHk9Ii44IiBzdHlsZT0iZm9udC12YXJpYW50LWNhcHM6bm9ybWFsO2ZvbnQtdmFyaWFudC1lYXN0LWFzaWFuOm5vcm1hbDtmb250LXZhcmlhbnQtbGlnYXR1cmVzOm5vcm1hbDtmb250LXZhcmlhbnQtbnVtZXJpYzpub3JtYWwiPkpTPC90c3Bhbj48L3RleHQ+PC9zdmc+&logoColor=FFFFFF" height=18></a>, a library that I previously developed for facilitating this kind of applications. It uses <b>Facemesh</b>
