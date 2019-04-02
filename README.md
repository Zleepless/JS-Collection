# JS-Collection
Collection of Javascript Code

//Password Validator
function isPasswordValid(input) {
  function hasUppercase(input) {
    for (i=0; i < input.length; i++) {
      if (input[i] === input[i].toUpperCase()) {
        return true;
      }
    }
  }
  function hasLowercase(input) {
    for (i=0; i < input.length; i++) {
      if (input[i] === input[i].toLowerCase()) {
        return true;
      }
    }
  }
  function isLongEnough(input) {
    return input.length >= 8;
  }
  function hasSpecialCharacter(input) {
    var specialCharacters = ['!', '@', '#', '$', '%', '^', '&', '*'];
    for (i=0; i<input.length; i++) {
      for (j=0; j<specialCharacters.length; j++) {
        if (input[i] === specialCharacters[j])
          return true;
      }
    }
  }
  if (hasUppercase(input) && hasLowercase(input) && isLongEnough(input) && hasSpecialCharacter(input)) {
    console.log('Valid');
  }
  if (!hasUppercase(input)) {
    console.log('Need Capital Letter');
	}
  if (!hasLowercase(input)) {
    console.log('Need Lower Letter');
	}
  if (!isLongEnough(input)) {
    console.log('Need 8 Letter');
	}
  if (!hasSpecialCharacter(input)) {
    console.log('Need Special Letter');
	}
}

isPasswordValid('Ahasdfg@'); //Test

//End of Password Validator
