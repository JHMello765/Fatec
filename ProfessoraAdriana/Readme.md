import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // 1. Idade em dias
        System.out.println("Digite anos, meses e dias de idade:");
        int anos = scanner.nextInt();
        int meses = scanner.nextInt();
        int dias = scanner.nextInt();
        int idadeEmDias = (anos * 365) + (meses * 30) + dias;
        System.out.println("Idade em dias: " + idadeEmDias);
        
        // 2. Percentual de votos
        System.out.println("Digite o número total de eleitores:");
        int totalEleitores = scanner.nextInt();
        System.out.println("Digite votos brancos, nulos e válidos:");
        int votosBrancos = scanner.nextInt();
        int votosNulos = scanner.nextInt();
        int votosValidos = scanner.nextInt();
        System.out.println("Brancos: " + (votosBrancos * 100.0 / totalEleitores) + "%");
        System.out.println("Nulos: " + (votosNulos * 100.0 / totalEleitores) + "%");
        System.out.println("Válidos: " + (votosValidos * 100.0 / totalEleitores) + "%");
        
        // 3. Reajuste salarial
        System.out.println("Digite o salário atual e o percentual de reajuste:");
        double salario = scanner.nextDouble();
        double percentual = scanner.nextDouble();
        double novoSalario = salario + (salario * percentual / 100);
        System.out.println("Novo salário: R$ " + novoSalario);
        
        // 4. Custo de um carro ao consumidor
        System.out.println("Digite o custo de fábrica do carro:");
        double custoFabrica = scanner.nextDouble();
        double custoFinal = custoFabrica + (custoFabrica * 0.28) + (custoFabrica * 0.45);
        System.out.println("Custo final ao consumidor: R$ " + custoFinal);
        
        // 5. Salário do vendedor
        System.out.println("Digite número de carros vendidos, total de vendas, salário fixo e comissão por carro:");
        int carrosVendidos = scanner.nextInt();
        double totalVendas = scanner.nextDouble();
        double salarioFixo = scanner.nextDouble();
        double comissaoCarro = scanner.nextDouble();
        double salarioFinal = salarioFixo + (carrosVendidos * comissaoCarro) + (totalVendas * 0.05);
        System.out.println("Salário final: R$ " + salarioFinal);
        
        // 6. Conversão de temperatura
        System.out.println("Digite a temperatura em Fahrenheit:");
        double fahrenheit = scanner.nextDouble();
        double celsius = (fahrenheit - 32) * 5/9;
        System.out.println("Temperatura em Celsius: " + celsius);
        
        // 7. Verifica se maior que 10
        System.out.println("Digite um número:");
        int valor = scanner.nextInt();
        System.out.println(valor > 10 ? "É MAIOR QUE 10!" : "NÃO É MAIOR QUE 10!");
        
        // 8. Positivo ou negativo
        System.out.println("Digite um número:");
        int num = scanner.nextInt();
        System.out.println(num >= 0 ? "Positivo" : "Negativo");
        
        // 9. Preço das maçãs
        System.out.println("Digite a quantidade de maçãs compradas:");
        int macas = scanner.nextInt();
        double preco = macas < 12 ? 1.30 : 1.00;
        System.out.println("Custo total: R$ " + (macas * preco));
        
        // 10. Média do aluno
        System.out.println("Digite as duas notas do aluno:");
        double nota1 = scanner.nextDouble();
        double nota2 = scanner.nextDouble();
        double media = (nota1 + nota2) / 2;
        System.out.println("Média: " + media);
        System.out.println(media >= 6 ? "Aprovado" : "Reprovado");
        
        // 11. Verificação de voto
        System.out.println("Digite o ano atual e o ano de nascimento:");
        int anoAtual = scanner.nextInt();
        int anoNascimento = scanner.nextInt();
        System.out.println((anoAtual - anoNascimento) >= 16 ? "Pode votar" : "Não pode votar");
        
        // 12. Maior valor
        System.out.println("Digite dois valores diferentes:");
        int a = scanner.nextInt(), b = scanner.nextInt();
        System.out.println("Maior: " + Math.max(a, b));
        
        // 13. Ordem crescente
        if (a > b) System.out.println(b + " " + a);
        else System.out.println(a + " " + b);
        
        // 14. Duração do jogo de xadrez
        System.out.println("Digite hora de início e fim do jogo:");
        int inicio = scanner.nextInt();
        int fim = scanner.nextInt();
        int duracao = (fim >= inicio) ? (fim - inicio) : (24 - inicio + fim);
        System.out.println("Duração: " + duracao + " horas");
        
        // 15. Salário com horas extras
        System.out.println("Digite horas trabalhadas no mês e salário por hora:");
        int horasTrabalhadas = scanner.nextInt();
        double salarioHora = scanner.nextDouble();
        double salarioTotal = (horasTrabalhadas <= 160) ? (horasTrabalhadas * salarioHora) : 
                              (160 * salarioHora) + ((horasTrabalhadas - 160) * salarioHora * 1.5);
        System.out.println("Salário total: R$ " + salarioTotal);
        
        // 16. Balanço do trimestre
        int jan = 15000, fev = 23000, mar = 17000;
        int total = jan + fev + mar;
        System.out.println("Gasto total: R$ " + total);
        System.out.println("Média mensal: R$ " + (total / 3));
        
        // 17. Média de LP1
        System.out.println("Digite P1, E1, E2, API, X e SUB:");
        double P1 = scanner.nextDouble(), E1 = scanner.nextDouble(), E2 = scanner.nextDouble(), 
               API = scanner.nextDouble(), X = scanner.nextDouble(), SUB = scanner.nextDouble();
        double mediaLP1 = (P1 * 0.6 + ((E1 + E2) / 2) * 0.4) * 0.5 + 
                          (Math.max(((P1 * 0.6 + ((E1 + E2) / 2) * 0.4) - 5.9), 0) / ((P1 * 0.6 + ((E1 + E2) / 2) * 0.4) - 5.9)) * (API * 0.5) + X + (SUB * 0.3);
        System.out.println("Média de LP1: " + mediaLP1);
        
        scanner.close();
    }
}
