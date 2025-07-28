# Mi-primer-juego-JAVASCRIPT
Aqui realiza mi primer juego como metodo de practica en JavaScript es un juego de adivinar un numero 
//estas son las variables 
let numeroPosible = 20;
let numeroSecreto = Math.floor(Math.random()*numeroPosible)+1;; 
let numeroUsuario = 0;
let intentos = 1;
//let palabraVeces = 'vez'; se comenta para utilizar codigo de template srcipt en la linea de codigo alert donde se muestra si se acerto o no
let maximosIntentos = 5;
while (numeroUsuario != numeroSecreto) {
    numeroUsuario = parseInt(prompt(`Me Indicas un número del 1 al ${numeroPosible} por favor:`));
    
    console.log(typeof(numeroUsuario));
    /*
    Este codigo realiza la 
    comparacion 
    */
    if (numeroUsuario == numeroSecreto) {
        //Si la condición se cumple 
        alert (`Acertaste, el número es: ${numeroUsuario}. lo hiciste en ${intentos} ${intentos == 1 ? 'vez' : 'veces'}`);
        } else {
            if (numeroUsuario > numeroSecreto) {
                alert('El numero secreto es menor');
            } else {
                alert('el numero secreto es mayor');
            }
            //Si no se cumple la condición
            //alert ('Lo siento, no acertaste el numero');
            //intentos = intentos + 1; esta es la forma detallada pero hay una mas reducida y viene de C++
            intentos++; 
            //palabraVeces = 'veces'; 
            if (intentos > maximosIntentos) {
            alert (`Llegaste al numero maximo de ${maximosIntentos} intentos`); 
            break; 

            }
        }
}      
