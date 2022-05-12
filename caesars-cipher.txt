function rot13(str) {
  const alphabet = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
let newStr = '';

for (let i = 0; i < str.length; i++){
  let Index = alphabet.indexOf(str[i]);
  if (Index == -1){
  newStr += str[i];
  } else {
    let newIndex = (Index + 13) % 26;
    newStr += alphabet [newIndex];
  }
}

return newStr;
}

rot13("SERR PBQR PNZC");