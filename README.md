
public class Troco {
    public static void main(String[] args) {
        int valorc, valorp, div5c, div5p, troco, cinquenta, dez, cinco;
        valorc = Entrada.leiaInt("Qual o valor da compra?");
        valorp = Entrada.leiaInt("Qual o valor pago? ");
        if (valorc == valorp){
            Entrada.escrever("Compra concluida");
        }else{
            if (valorp >= valorc){
                if (valorc > 0 && valorp > 0){   
                div5c = valorc % 5;
                div5p = valorp % 5;
                    if (div5p == 0 && div5c ==0){
                
                        troco = valorp - valorc;
                        cinquenta = (int) (troco / 50) ;
                
                        dez = troco - 50 * cinquenta;
                        dez = (int) (dez / 10);
                
                        cinco = troco - (dez * 10 + cinquenta * 50);
                        cinco = (int) (cinco / 5);
                
                        Entrada.escrever("O troco será composto de:\n"+cinquenta+" nota(as) de cinquenta reis.\n"+dez+" nota(as) de dez reais\n"+cinco+" nota(as) de cinco reais");
                    }else{
                        Entrada.escrever("Troco não é possivel");
                    }
                }else{
                    Entrada.escrever("Valor da compra ou do pagamento negativo");
                }   
            }else{
                Entrada.escrever("Compra recusada: Falta dinheiro");
            }
            System.exit(0);
        }
    }
}
