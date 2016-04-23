# Exercicio_1
Implementação do programa calculadora

public class Calc {
	int value, keep;
	char toDo;
		
	void add(){
		keep = value;
		value = 0;
		toDo = '+';
	}
	
	void subtract(){
		keep = value;
		value = 0;
		toDo = '-';
	}
	
	void multiply(){
		keep = value;
		value = 0;
		toDo = '*';
	}
	
	void divide(){
		keep = value;
		value = 0;
		toDo = '/';
	}
	
	void compute(){
		if(toDo == '+')
			value = keep + value;
		else if(toDo == '-')
			value = keep - value;
		else if(toDo == '*')
			value = keep*value;
		else if(toDo == '/')
			value = keep/value;
		keep = 0;
	}
	
	void clear(){
		keep = 0;
		value = 0;
	}
	
	void digit(int x){
		value = value*10 + x;
	}
	
	int display(){
		return value;
	}
	
	Calc(){
		clear();
	}
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Calc c = new Calc();
		c.digit(1);
		c.digit(3);
		c.add();
		c.digit(1);
		c.digit(1);
		c.compute();
		System.out.println(c.display());
	}
		
}
