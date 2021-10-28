## submitting data
to get your spotify data, request it from the spotify website. (google it.) it says it should arrive within 30 days but it's usually around 3. when it's done you'll get a zip file with json files in it. download this and:

1. unzip the zip folder
2. in the unzipped folder, delete all the files except for the stream history files, which are of the form `StreamingHistoryX.json` where `X` is a number from `0` to `n` if you have `n+1` files. note: the reason we ask you to delete everything except the stream history is that some of the data is personal (e.g., payment information etc.)
3. re-zip this folder and name the zip file `firstname_lastname.zip`
4. fork the repo and put your zip file in the `zips` folder
5. make a pull request from your branch with the comment "data submission"

pull requests will be reviewed promptly and then the data will be added to our dataset for use in analysis.

you can look at the contents of this folder for examples on how to upload your data.