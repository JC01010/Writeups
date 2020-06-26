**I-wanna-get-the-flag (rev, 34 solves, 492 points)**

Looking through the files after decompiling the the game with Altar, we find a file named rWinner.json in the ROOM folder. The file contained a set of coordinates in the format:

```
{"pos":{"x":658,"y":422},"bg":"bAllTiles","sourcepos":{"x":32,"y":96},"size":{"width":32,"height":32},"scale":{"x":1.0,"y":1.0},"colour":"#FFFFFFFF","tiledepth":1000000,"instanceid":10001585},{"pos":{"x":633,"y":422},"bg":"bAllTiles","sourcepos":{"x":32,"y":96},"size":{"width":32,"height":32},"scale":{"x":1.0,"y":1.0},"colour":"#FFFFFFFF","tiledepth":1000000,"instanceid":10001586},{"pos":{"x":631,"y":422},"bg":"bAllTiles","sourcepos":{"x":32,"y":96},"size":{"width":32,"height":32},"scale":{"x":1.0,"y":1.0},"colour":"#FFFFFFFF","tiledepth":1000000,"instanceid":10001587}, ...
```

We take a list of all the coordinates, and use notepad++ to replace ```{"pos":``` with ```\n {"pos":```, and paste the json file into a google spreadsheet (https://docs.google.com/spreadsheets/d/1OkEBMrkrcqY2bnlF_rw5eWxopSJmVG4ltTzuTdzOo4Q/edit#gid=0).

We format the spreadsheet into a list of coordinates, and paste it into desmos. However, the flag was flipped about the x axis, so I simply replaced the y coordinates of each point with 576-y.

The resulting graph is shown here: https://www.desmos.com/calculator/yqucn2r7en

flag: flag{gms_succs_kiddo}
