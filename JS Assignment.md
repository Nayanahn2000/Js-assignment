1. Write a function in Javascript to find maximum element in an array?

function findMax(arr) {
    // Check if the array is empty
    if (arr.length === 0) {
        return undefined; // Return undefined if the array is empty
    }

    let max = arr[0]; // Assume the first element is the maximum

    // Iterate through the array starting from the second element
    for (let i = 1; i < arr.length; i++) {
        // Update max if the current element is greater
        if (arr[i] > max) {
            max = arr[i];
        }
    }

    return max; // Return the maximum element
}

// Example usage:
let numbers = [3, 7, 2, 8, 5];
console.log(findMax(numbers));

2. Write a function to sort an array of string in alphabetic order

function sort(arr) {
    arr = arr.split("");
    for (i = 0; i < arr.length; i++) {
        for (j = 0; j < arr.length; j++) {
            if (arr[j] > arr[i]) {
                temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
    }
    return arr.join("");
}
console.log(sort("dcna"));

3. Write a Javascript function which helps to sum of all the array element 

function sumArrayElements(arr) {
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }
    return sum;
}

// Example usage:
let numbers = [1, 2, 3, 4, 5];
console.log(sumArrayElements(numbers));

4. Write a Javascript function to remove elements from the array which is not divisible by 2

function removeNonDivisibleByTwo(arr) {
    let result = []; // Create an empty array to store elements divisible by 2
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] % 2 === 0) { // Check if the element is divisible by 2
            result.push(arr[i]); // Add the element to the result array
        }
    }
    return result;
}

// Example usage:
let numbers = [1, 2, 3, 4, 5, 6];
console.log(removeNonDivisibleByTwo(numbers));