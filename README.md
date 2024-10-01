# Flow angle identification challenge

## Problem Summary
In this challenge, the goal is to identify the flow angle for each image and write it to a csv file.

## Instructions to use the algorithm:

- It is mandatory having the following libraries installed in your python environment: opencv-python, pytesseract and numpy. You can do this by executing "pip install opencv-python pytesseract numpy"

- The images to be analyzed must be in the folder "images/". (or you can change it by changing the variable "images_folder" value path)

- Every generated csv file will be stored in the folder "csv_results/" (or you can change it by changing the variable "csv_files_path" value path).The csv filename will be the current date in which the algoritm runs and with the following format: YYYY-MM-DD.

- The algorithm works in the following manner: everytime the user runs the algorithm, it looks inside the images folder ("images/" or the customized one), processes each image and, for each image, it returns the numeric values inside it. It will not be automatically processed with the arrival of new image files in the folder. In other words, you'll need to run the algorithm manually every time you consider necessary (and it will process all the images inside the images folder, generating the csv file at the end).After each result, the algorithm writes the numeric values into the csv file (stored in "csv_results/" folder or the customized one). The registered values are: timestamp, filename, angle1, angle2 and total(angle's sum).If an entry already exists in the csv file, i.e, if the file contains a row with the same filename, same angle1, same angle2 and same total as the new data, it'll be ignored. You can delete the csv file at any time and generate it again almost instantaneously, depending on the number of file images inside the folder.