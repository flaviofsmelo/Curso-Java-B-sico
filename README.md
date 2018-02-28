# Curso-Java-B-sico
package com.loiane.cursojava.aula15;

import java.util.Scanner;

public class Exercicio12 {

	public static void main(String[] args) {
		
		Scanner scan = new Scanner(System.in);
		
		System.out.println("Entre o valor da hora trabalhada: ");
		double valor = scan.nextDouble();
		
		System.out.println("Entre a quantidade de horas trabalhadas: ");
		double hora = scan.nextDouble();
		
		double salarioBruto = valor * hora;
				
		//descontos
		int percentualIR = 0;
		if (salarioBruto <= 900) {
			System.out.println("Isento");
		} else if (salarioBruto > 900 && salarioBruto <= 1500) {
			percentualIR = 5;
		} else if (salarioBruto > 1500 && salarioBruto <= 2500) {
			percentualIR = 10;
		} else if (salarioBruto > 2500) {
			percentualIR = 20;	
		}	
		
		double impostoRenda = (salarioBruto /100) * percentualIR;
		double sindicato = (salarioBruto /100) * 3;
		double inss = (salarioBruto /100) * 10;
		double fgts = (salarioBruto /100) * 11;
		
		double totalDescontos = impostoRenda + sindicato + inss;
		double salarioLiquido = salarioBruto - totalDescontos;
		
		System.out.println("Salário Bruto: R$ " + salarioBruto);
		System.out.println("IR ("+ percentualIR + "%) " + impostoRenda);
		System.out.println("Desconto sindicato: R$ " + sindicato);
		System.out.println("INSS: R$ " + inss);
		System.out.println("FGTS: R$ " + fgts);
		System.out.println("Total de descontos: R$ " + totalDescontos);
		System.out.println("Salário líquido: R$ " + salarioLiquido);	
		}
		
 
}
