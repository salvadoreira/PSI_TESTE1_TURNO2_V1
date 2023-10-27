# Teste de PSI 1 - Turno 2 - Versão 1

## Informação do aluno

    Nome: Salvador Oliviera Amôedo da Eira

Teste termina às 13:25.

Escreve as respostas dentro dos blocos correspondentes.
Substitui as reticências pelo que é pedido em cada pergunta.
Não desformates o documento.

### P1. Indica o que é impresso pelo seguinte código. Justifica a tua resposta

    bool x = true && false;
    x |= 2 < 5;
    
    Console.WriteLine(x);

P1 - A saida do código será True, porque na booleana x quer saber se o valor de x é verdadeiro ou falso, e como o valor de x é 2 menor que 5, a saida do código será True

    ...

### P2. Considera o seguinte código com um *bug*

    short s = long.MaxValue;

    Console.WriteLine(s);

### Indica uma possível correção para que o código não apresente erros. Explica porque foi necessário fazer essa correção

P2 - Resposta

    short s = (short)long.MaxValue;

    Console.WriteLine(s);

    Tivemos que converter o valor máximo de long em um short porque o valor maximo do long é maior que o valor maximo do short.
 


### P3. Escreve um programa que solicite ao utilizador dois números reais e apresente o resultado do primeiro (base) elevado ao segundo (expoente). Não podes usar um método da classe Math para obter o resultado

P3 - using System;

class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Calculadora de Potência");
        Console.Write("Digite a base (número real): ");
        double baseNumber = double.Parse(Console.ReadLine());

        Console.Write("Digite o expoente (número real): ");
        double expoent = double.Parse(Console.ReadLine());

        double result = CalculatePower(baseNumber, expoent);

        Console.WriteLine($"Resultado: {result}");
    }

    static double CalculatePower(double baseNumber, double expoent)
    {
        double result = 1.0;

        if (expoent >= 0)
        {
            for (int i = 0; i < expoent; i++)
            {
                result *= baseNumber;
            }
        }
        else
        {
            for (int i = 0; i > expoent; i--)
            {
                result /= baseNumber;
            }
        }

        return result;
    }
}
    

### P4. Estás na pasta raiz do teu repositório local, onde atualizaste um ficheiro de nome 'Classes.cs'. Queres enviar **apenas** esta atualização para o teu repositório remoto. Indica os comandos necessários. A mensagem de commit deve ser apropriada

P4 - Resposta

    Os comandos necessários são: git status, git add Classes.cs, git commit -m "Atualização do arquivo 'Classes.cs'", git push

