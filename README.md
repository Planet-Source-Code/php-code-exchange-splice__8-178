<div align="center">

## Splice


</div>

### Description

Create a 2 dimentional array (rows and columns) out of a semicolon delimited text file. by Travis Barney
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[PHP Code Exchange](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/php-code-exchange.md)
**Level**          |Intermediate
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |PHP 3\.0, PHP 4\.0
**Category**       |[Files](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files__8-2.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/php-code-exchange-splice__8-178/archive/master.zip)





### Source Code

```
/* ------ Code -------------------------------- */
function splice($filename){
 if(file_exists($filename)){
  global $value; $value=array("0"); // clear the array.
  $rows=file($filename); // break text file into a rows array
  for($num=0;$num < count($rows); ++$num){
   $column=split(";",$rows[$num]);
   $value[$num]=$column;}}}
/* ------ Notes --------------------------------
 Useage:
 1) create a ; delimited text file.. ie:
  r1c1;r1c2;r1c3;r1c4;r1c5
  r2c1;r2c2;r2c3;r2c4;r2c5
  r3c1;r3c2;r3c3;r3c4;r3c5
  r4c1;r4c2;r4c3;r4c4;r4c5
  r5c1;r5c2;r5c3;r5c4;r5c5
  r6c1;r6c2;r6c3;r6c4;r6c5
 2) save it what you like..
  example.txt
 3) run the splice function..
  splice("example.txt")
 4) access the values of the array..
  echo $value[3][4];
  will print: r3c4
Would be good for a flat file text database type of system.
  -------------------------------------------- */
```

