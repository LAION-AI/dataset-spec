# dataset-spec
Check out this video: https://www.youtube.com/watch?v=cmVBaShtygA

## Metadata for image/text datasets

If the dataset can be downloaded from image urls, 
Prefer distributing data publicly (eg on huggingface) as parquet files with these columns:
* URL
* TEXT
If other information is available, feel free to provide it was well in other columns

## Image-Text-Datasets

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

If you have a VQA - dataset, put the prefix "Q: " before the question & the prefix "A: " before the answer and then concatenate both texts. Put those into the "txt" field.
Also out an entry into the "json" field with the key "question" & the question as value. Also add an entry with the key "answer" to the json with the answer as the value.

A help to create wds tar files from jpg & txt files can be this script: [wds_create_shards.py](wds_create_shards.py) (**json support added, you can use the --json tag to automatically read json files and add them to the tar files 04-19-2022**)

|  Dataset info  |  Who works on it  |
|---|---|
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 
|   |   | 


