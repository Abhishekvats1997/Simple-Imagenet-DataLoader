# Simple-Imagenet-DataLoader

When using the Imagenet Dataset for training/evaluating your models there is quit a bit of confusion involved as there are different directory structures of the dataset in diff version which makes loading the dataset a bit difficult.

Also, different classes have their images in different folders with names which have no apparent relation to their label number in the 1000 classes that the dataset has.

I wrote a custom dataloader for PyTorch which simplifies this process for some of few.

There are two variants of Imagenet with directory structure as follows
- train and val both folders have images in subfolders.
- train has images in subfolders while val has all the images present as is without any subfolders.

