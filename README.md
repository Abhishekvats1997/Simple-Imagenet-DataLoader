# Simple-Imagenet-DataLoader

When using the Imagenet Dataset for training/evaluating your models there is quit a bit of confusion involved as there are different directory structures of the dataset in diff version which makes loading the dataset a bit difficult.

Also, different classes have their images in different folders with names which have no apparent relation to their label number in the 1000 classes that the dataset has.

I wrote a custom dataset class for PyTorch which simplifies this process for some of few.

There are two variants of Imagenet with directory structure as follows
- train and val both folders have images in subfolders. (Type 1)
- train has images in subfolders while val has all the images present as is without any subfolders. (Type 2)

## Sample Usage Type 1
```
from ImageNet import ImageNet
```
```
dataset = ImageNet(data_dir,transforms)
```

##Sample Usage Type 2
```
from ImageNet import ImageNetFull
```
```
dataset = ImageNetFull(data_dir,transforms)
```

## Note
- There are a few scripts available online which modify the directory structure of your dataset into a suitable one for the default Pytoch Dataloader but if run incorrectly it can ruin your entire dataset and the Fll ImageNet dataset being 165gb is a pain to redownload aur even extract.
- The labels returned by this implementation are the actual classification labels and hence no additional code is required while calculating the loss and accuracy in the training loop 