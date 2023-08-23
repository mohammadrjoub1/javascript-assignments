# day 11  2023-8-22
# Types section:
- video#1:think deeply about JavaScript and understand its behaviour.
- video#2:the type of operator always return a string that contain the type of the variable even undefined or null always ahs to be in double quetes "" ""
- video#3:how BigInt differs from other numbers in JavaScript.
- video#4:various ways something can be empty in JavaScript: undefined, undeclared, and uninitialized.
- video#5: NAN===NAN is false and NAN- + * / 5 = NAN always!
- video#6:explains how operations on it can cause unexpected results.
# Coercion section:
### He provided an in-depth exploration of abstract operations in JavaScript, elucidating the language's nuanced approach to handling them and shedding light on its idiosyncratic and at times unpredictable behaviors within this context.



# deliverables:
## QUESTION 1:
function convertStringToNumber(item) {

    if (typeof (item) === 'string') {

        return +item;

    }
    else {


        return {

            value: item,
            type: typeof (item)
        };
    }


}
## QUESTION 2:
function checkNaN(item) {

    if (item !== item) {// the only case an number is nan is nan !== nan

        return true // so item is nan

    }
    else {
        return false;
    }

}
## QUESTION 3:
function isEmptyValue(item) {
    if (Boolean(item)) {


        return true;// its an null or undefined or empty string
    }
    return false;
    

}
## QUESTION 4:
function compareObjects(ob1,ob2) {

    if (typeof (ob1) !== "object" || typeof (ob2) !== "object") {


        return [ob1, ob2];
    }
    else {

        return Object.is(ob1, ob2);

    }




}
## QUESTION 5:
function complexCoercion(input) {
    if (typeof input === "number") {
        return Boolean(input.toString());
    } else if (typeof input === "string") {
        return Boolean(input);
    } else if (input === null || input === undefined) {
        return false;
    } else {
        return input;
    }
}

