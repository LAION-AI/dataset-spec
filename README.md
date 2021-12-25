# dataset-spec
Describe the format of image/text datasets

## spec

The format is a collection of tar files (that dataset format is called webdataset) containing images, captions and metadata

* 00000.tar of size 270MB containing at most 10k samples
  * 0.jpg
  * 0.txt containing the caption
  * 0.json containing metadata such as the url, the original width, the exif data, whether the image is NSFW
