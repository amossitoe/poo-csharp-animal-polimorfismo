Classe Animal e derivadas Cachorro, Gato e Vaca com método Falar().

*******************************************************************************/
using System;
class Animal {
    
    protected string nome;
    protected int idade;
    
    public Animal(string nome, int idade){
        this.nome=nome;
        this.idade=idade;
    }
    public virtual void falar(){
        Console.WriteLine("O animal emite um som");
    }
    public void mostrarDados(){
        Console.WriteLine($"Nome: {nome} | Idade: {idade} anos");
    }
}
    class Cachorro:Animal{
        
        public Cachorro(string nome, int idade):base(nome, idade){
    }
    public override void falar(){
        Console.WriteLine($"O Cachorro {nome} late: Au au au!");
    }
    }
    class Gato:Animal{
        
        public Gato(string nome, int idade):base(nome, idade){
    }
    public override void falar(){
        Console.WriteLine($"O Gato {nome} mia: Miau!");
    }
    }
    class Vaca:Animal{
        
        public Vaca(string nome, int idade):base(nome, idade){
    }
    public override void falar(){
        Console.WriteLine($"A Vaca {nome} muge: Muuu!");
    }
    }

    class AnimalTeste{
  static void Main(string[]args) {
      
     Animal [] animais={new Cachorro("Maçãnzinha", 3), new Gato("Liroy", 2), new Vaca("Mimosa", 4)};
  
  for(int i=0; i<animais.Length;i++){
      animais[i].mostrarDados();
      animais[i].falar();
  }
}
}
