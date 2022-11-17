*Console-Finances 

Objective of this project is to write a block of code that would dynamically calculate and analyzes the records of an array of data. see the screen shot below:



![alt text](/img/scr1.png)



The dataset composed of 2 dimantional arrays set with two data field, which is: 
    - Date 
    -and Profit/Losses.

I was tasked with analyzing the records to calculate each of the following:

 - The total number of months included in the dataset.

    // Iterate over the array and intrement by 1 to get the total number of months in the array
    ar totalMonth = 0;
    for (var i = 0; i < finances.length; ++i) {
    totalMonth += 1;
    }

 - The net total amount of Profit/Losses over the entire period.

        /*

            - Create total place holder 
            - Put all the figures into one array; start by:
                - create an empty array
                - Loop over the sub arrays figuers 
                    - push it to empty array
                

                - Write another loop to loop over the new array
                - then add the figures to total sum to get the lose/profile
        */

        // This solution worked out lot more simpler
        var profitLossTotal = 0;
        for (var arrayIndex = 0; arrayIndex < finances.length; arrayIndex++) {
            profitLossTotal += finances[arrayIndex][1];
        }

 - The average of the **changes** in Profit/Losses over the entire period.
        -  create a total prace holder
        - subract figers from month to month 
        - Then find the average by deviding the tital with number of month i.e.
            total/number of month
        
        

var

    tempfigureHolder,
    negArray = [],
    posArray = []
    ;

// Array seperating the positive and negative values
for (var i = 0; i < finances.length; i++) {

    if (finances[i][1] < 0) {
        negArray.push(finances[i][1]);
    } else {
        posArray.push(finances[i][1]);
    }

}
// console.log(posArray + "\n\n"); 

// Looping throught the pogative array to find the differences

// Positive value variables
var

    posDiffTempPlaceHolder,
    posDiff = [],
    posTotal = 0;

for (var i = 0; i < posArray.length; i++) {

    //  * Line below code checking to if there is next incremental item if false then return 0
    var nextTotal = (posArray[i + 1] || 0) && posArray[i + 1];
    posDiffTempPlaceHolder = (posArray[i] > nextTotal) ? posArray[i] - nextTotal : nextTotal - posArray[i];
    posDiff.push(posDiffTempPlaceHolder);

}
posDiff.pop(); 
for (var i = 0; i < posDiff.length; i++) {

    posTotal += posDiff[i];

}
// console.log("Pos array " + posArray); 
// console.log(posDiffTempPlaceHolder); 
// console.log(posDiff)
// console.log(posTotal); 

// Negative value variables
var

    negDiffTempPlaceHolder,
    negDiff = [],
    negTotal = 0;

for (var i = 0; i < negArray.length; i++) {

    //  * Line below code checking to if there is next incremental item if false then return 0
    var nextTotal = (negArray[i + 1] || 0) && negArray[i + 1];
    negDiffTempPlaceHolder = (negArray[i] > nextTotal) ? negArray[i] - nextTotal : nextTotal - negArray[i];
    negDiff.push(negDiffTempPlaceHolder);

}

negDiff.pop(); 
for (var i = 0; i < negDiff.length; i++) {

    negTotal += negDiff[i];

}

// Total average
avgTotalSum = 0; 
avgTotalSum = posTotal - negTotal; 
var avarage = avgTotalSum / totalMonth; 

 - The greatest increase in profits (date and amount) over the entire period.
 
 - The greatest decrease in losses (date and amount) over the entire period.

 The greatest increase in profits (date and amount) over the entire period.
    - Find the highest number 
    - and then get console both date and the value 
        // var testing =[1,2,3,4,5,6,71; 
        newArray = [];
        var increased = 0;
        var maxValue = [];
        var minValue = "";

        for (var i = 0; i < finances.length; i++) {
            newArray.push(finances[i][1]);
            // get both value if it is the greatest value
        }

        var max = Math.max(...newArray);
        var min = Math.min(...newArray);
        for (var i = 0; i < finances.length; i++) {
            if (finances[i][1] === max) {
                maxValue = finances[i];
                console.log("max value", maxValue);

            }
            else if (finances[i][1] === min) {
                minValue = finances[i];
                //console.log(min);
                break;
            }
        }

        ** Console output: 
         



![alt text](/img/con_output.png)



Thank you and I hope you found the code interesting!
