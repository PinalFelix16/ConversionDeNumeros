# ConversionDeNumeros
Conversión de un numero decimal a: BINARIO, HEXADECIMAL, OCTAL.

import javax.swing.*;

public class SistemasNumericos {
    public static void main(String[] args) {
        String numeroStr=JOptionPane.showInputDialog(null,"Ingrese un numero entero");

        int numeroDecimal=0;

        try {
            numeroDecimal=Integer.parseInt(numeroStr) ;
        }catch (NumberFormatException e){
            JOptionPane.showMessageDialog(null,"debes ingresar un numero entero");
            main(args);
            System.exit(0);
        }

        String resultadoBinario="numero Binario = " + numeroDecimal + " = " + Integer.toBinaryString(numeroDecimal);

        String resultadoOctal="numero Octal = " + numeroDecimal + " = " + Integer.toOctalString(numeroDecimal);

        String resultadoHex="numeroHex = " + numeroDecimal + " = " + Integer.toHexString(numeroDecimal);

        String mensaje= resultadoBinario;
        mensaje+="\n" + resultadoOctal;
        mensaje+="\n" + resultadoHex;
        JOptionPane.showMessageDialog(null, mensaje);
    }
}
