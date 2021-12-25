# dataset-spec
Describe the format of image/text datasets

## spec

The format is a collection of tar files (that dataset format is called webdataset) containing images, captions and metadata

* 00000.tar containing 10k samples
  * 0.jpg
  * 0.txt containing the caption
  * 0.json containing metadata such as the url, the original width, the exif data, whether the image is NSFW


If the biggest dimension of an image is bigger than 512, then resize so that the biggest dimension would be 512 and keep the aspect ratio.

If the smallest dimension of the image is below 64, drop the sample.

Do not increase the resolution of the sample if it is below 512, but above 64, just keep it.

Save the image data in the webdataset format as JPEG highest quality.

Use “jpg” as field for the image and “txt” as field for the caption.
A "json" field should contain at least height and width of the image, eventually if more data is available.


|   |   |   |   |   |
|---|---|---|---|---|
|   |   |   |   |   |
|   |   |   |   |   |
|   |   |   |   |   |
