--- 
layout: single
title: "How to Obtain Multiple File Paths from a Folder for Use in a Python Program"
date: 2021-09-01
comments: true
show_date: true
toc: true
toc_icon: "cog"
excerpt: ""
header:
  overlay_image: /images/code-01.jpg
  overlay_filter: rgba(155, 150, 160, 0.5)
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
  actions : 
    - label: "More Info"
      url: "https://cyrillemesue.github.io/getting-all-files-from-folder/"
--- 
Here is a code to obtain all image paths for a folder for your datascience project

```python

import os
    
# define the directory where the images are located      
images_path = "PATH"

img_paths = sorted([os.path.join(images_path, fname) for fname in os.listdir(images_path)
                                      if fname.endswith(".jpeg") and not fname.startswith(".")]) # replace ".jpeg" with the format in which the image file is.
                                      
# img_paths is a list of all image paths in the PATH directory.
```
       
