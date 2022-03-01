# Anotações da linguagem Java

### Instalar openJDK
 - Acessar https://www.azul.com/downloads procurar versão LTS, nessa data foi java 11 para Windows 64bit
 - Baixar arquivo .zip
 - Criar uma pasta dentro de c:\Arquivos de programas chamada Java
 - Extrair o arquivo .zip dentro da pasta java
 - Incluir JAVA_HOME nas variáveis de ambiente passando caminho da pasta extraída em java criada anteriormente
 - Adicionar o caminho ao path adicionando ao final do caminho um \bin
 - No cmd digitar java –version para ver se Windows reconhece o openjdk

### Testando compilador e lendo arquivo .class
 - Crie um arquivo OlaMundo.java e acesse a pasta dele com cmd
 - No arquivo digite o seguinte código
 - - //Minha Primeira Classe Java
 - - Class OlaMundo {               
 - - public static void main(String[] args) {  
 - - System.out.println(“Hello, Word Java!!!!”); 
 - - }
 - - }
 - No cmd digite javac OlaMundo.java 
 - O comando anterior vai criar o arquivo OlaMundo.class
 - No cmd digite java OlaMundo
 - No cmd será escrito a mensagem Hello, Word Java!!!!

### Instalando IDE Eclipse
 - Acesse https://www.eclipse.org/downloads/
 - Clicar em downloads
 - instalar executavel

### Variáveis
 - <Visibilidade> <modificador> <tipo> <nome> = <valor inicial>
 - - Visibilidade
 - - - public
 - - - protected
 - - - private
 - - Modificador
 - - - static
 - - - final
 - - Tipo de dado
 - - -  int
 - - - double
 - - - boolean
 - - Nome
 - - Valor Inicial
 - Convenções e regras
 - - Nome Não deve começar com numero, evite usar $ e _ no inicio, case-sensitive, não deve ter espaço não po ser paravra reservada 
 - Boas Praticas
 - - Nome sempre começa com letra minuscula, notação camelo onde segunda palavra inicia com maiuscula, quando constante (final) todas maiuscula e separada por _

 ### Operadores
  - Pós-fixado x++ e x--
  - Pré-fixado ++x e --x
  - Aritiméticos +, -, *, / e %
  - atribuição =, +=, -=, *=, /= e %=

  ### Conversões (casting)
   - Upcast (implicito), não costuma dar problemas, pois consiste em colocar um dado menor em um espaço maior ex. int i = 10 vai para long l com atribuição de l = i
   - Downcast (explicito), pode dar problemas, pois consistem e colocar um dado maior em espaço menor ex. float f = 10.5f vai para int i com atribuição i = (int) f;

### Métodos
 - <visibilidade> <tipo> <modificador> <retorno> <nome> (<paramentros>) <exceções> <corpo>
 - - Visibilidade
 - - - public - em qualquer lugar
 - - - protected - dentro da classe, mesmo pacote e subclasse
 - - - private - só dentro da classe
 - - Tipo
 - - - concreto
 - - - abstrato
 - - Modificador
 - - - static
 - - - final 
 - - Retorno
 - - - Tipo de dado
 - - - void
 - - Nome -> usa mesma regra de variavel
 - - Parametros

 - Chamar método
 - - Classe.metodo()

### Sobrecarga
 - Consiste em criar metodos com mesmo nome mas com execuções diferentes dentro do mesmo contexto, exemplo você pode criar um metodo para calcular area de figura geometricas, o metodo poderia chamar calcularArea para calcular area de um triagulo, receberia 1 parametro e faria o calculo, um metodo com mesmo nome poderia ser criado para calcular area de um quadrado recebendo 2 parametros e calculando como tal e assim sucessivamente.

### Retornos
 - Métodos podem o não retornar algo, para retornar usamos return ex. -> public int numeroDez() { return 10;}  

### Operadores relacionais
 - igual ==
 - diferente !=
 - maior >
 - maior igual >=
 - menor <
 - menor igual <=

### Operadores Logicos
 - conjunção -> e (and) &&
 - disjunção -> ou (or) ||
 - Disjunção exclusiva -> xor ^
 - negação -> inversão !

### Controle de Fluxo
 - Decisão: if, if-else, if-else-if, switch e operador ternário
 - Repetição: for, while, do while
 - Interrupção: break, continue e return


### Orientação a Objetos
 - Paradigma orientado a objeto tem representação mais realista
 - Foca na modelagem e na interação
 - foca no que fazer
 - melhor coesão
 - melhor acoplamento
 - diminuição de gap semantico
 - coletor de lixo

 - Fundamentos POO
 - - Abstração
 - - Reuso
 - - Encapsulamento
 
 - Classe
 - - Uma classe é a abstração do objeto do mundo real é o modelo
 - - Nome da classe nomalmente é um substantivo ex. bola, carro, loja
 - Atributos
 - - Atributos são as caracteristicas da classe
 - - ex. cor, peso, altura, valor, etc
 - Método
 - - Ação que a classe pode realizar
 - - ex. rolar, buzinar, abrir, fechar, desligar etc.

 ### Relações
  - Herança -> usado para criar subtipos ex. class Carro extends Veiculo
  - - Tipos
  - - - Simples
  - - - Múltipla

  - - Polimorfismo
  - - - mesma ação se comportando diferente

  - - Sobrescrita
  - - - mesma ação podendo se comportar diferente

  - Associação
  - - Estrutural
  - - - Composição
  - - - Agregação
  - - Comportamental
  - - - Dependência

  - Interface -> usado para implementar metodos 

  ### Pacotes
   - Ajuda a organizar as classes
   - Projeto -> SRC -> br -> com -> site

### Debugging
 - Debugar é analisar o codigo linha a linha com ajuda de uma IDE, similar ao teste de mesa

### Tratamento de Exceções
 - Error - Não tem como tratar
 - Unchecked - não é obrigado a tratar
 - Checked Exception - obrigado a tratar com try, catch, finally
 
### Coleções
 - Criar uma lista -> List<Double> minhaLista = new ArrayList<Double>();
 - Adicionar elementos -> minhaLista.add(5.5);
 - Adicionar elementos e uma determinada posição-> minhaLista.add(posição, 5.5);
 - Imprimir -> System.out.println(minhaLista); ou  System.out.println(minhaLista.toString);
 - Exibir posição dentro de uma lista -> minhaLista.indexOf(5.5);
 - Substituir elemento -> minhaLista.set(posição, valor);
 - verifica se tem elemento na lista -> minhaLista.contains(5.5);
 - imprimir lista com for -> for (Double lista : minhaLista) System.out.println(lista);
 - Pegando item da lista pelo indice -> minhaLista.get(0); (pega primeiro item)
 - Pegar menor valor -> Collection.min(minhaLista);
 - Pegar maior valor -> Collection.max(minhaLista);
 - somar valores:
 - - Iterator<Double> interator = notas.iterator();
 - - Double soma = 0d;
 - - while(iterator.hasNext()) {
 - - - Double next = iterator.next();
 - - - soma += next;
 - - }
 - Quantidade de elementos -> minhaLista.size();
 - Remover elemento -> minhaLista.remove(valor) ou minhaLista.remove(indice)
 - Remover valores menores que 7:
 - - Iterator<Double> interator = notas.iterator();
 - - while(iterator.hasNext()) { (verifica se tem proximo na lista)
 - - - Double next = iterator.next();
 - - - if (next < 7 >) iterator.remove();
 - - }
 - Apagar toda lista -> minhaLista.clear()
 - verificar se a lista tem elementos -> minhaLista.isEmpty();

 #### Exemplo de utilização de lista com objeto

 1) Criar uma classe Gato com seguites atributos nome, idade e cor

 public class Gato {
    String nome;
    Integer idade;
    String cor; 
 }

 2) criar metodos gets
 3) sobrescrever toString
 @Override
 public String toString() {
    return "{"
    "nome='" + nome + '\'' + 
    ", idade=" + idade +
    ", cor'" + cor + '\'' +
    '}';
 }

4) criar a lista dentro do main
List<Gato> meusGatos = new ArrayList<>() {{
   add(new Gato(nome: "jon", idade:18, cor:"preto"));
   add(new Gato(nome: "pedro", idade:7, cor:"branco"));
   add(new Gato(nome: "Simba", idade:6, cor:"tigrado"));
   add(new Gato(nome: "jon", idade:12, cor:"amarelo"));
}}

5) imprimir lista -> System.out.println(meusGatos);

6) Agora é brincar com a lista:
 - Imprimir lista em ordem aleatoria -> Collections.shuffle(meusGatos);
 - Comparar itens da lista -> implementar interface Comparable
 class Gato implements Comparable<Gato>
 - Sobrescrever o metodo compareTo
 public int compareTo(Gato gato) {
    return this.getNome().compareToIgnoreCase(gato.getNome());
 }

 - Organizando gatos por ordem natural (nome) -> Collections.sort(meusGatos);
 
 - Organizando gatos por idade, precisa criar uma nova classe para isso
 class ComparadorIdade implements Comparator<Gato> {
    @Override
    public int compare(Gato g1, gato g2) {
       return Integer.compare(g1.getIdade(), g2.getIdade());
    }
 }
 - listando gatos por idade -> Collections.sort(meusgatos, new ComparatorIdade()) ou meusGatos.sort(new ComparadorIdade());

 - Organizando gatos por cor, também precisa criar uma nova classe para isso
 class ComparadorCor implements Comparator<Gato> {
    @Override
    public int compare(Gato g1, gato g2) {
       return g1.getCor().compareToIgnoreCase(g2.getCor());
    }
 }
 - listando gatos por cor -> Collections.sort(meusgatos, new ComparatorCor()) ou meusGatos.sort(new ComparadorCor());

 - Organizando gatos por nome, depois cor e depois idade, também precisa criar uma nova classe para isso
 class ComparadorNomeCorIdade implements Comparator<Gato> {
    @Override
    public int compare(Gato g1, gato g2) {
       int nome = g1.getNome().compareToIgnoreCase(g2.getNome());
       if (nome != 0) return nome;

       int cor = g1.getCor().compareToIgnoreCase(g2.getCor());
       if (cor != 0) return cor;

       return Integer.compare(g1.getIdade(), g2.getIdade());
    }
 }
 - listando gatos por cor -> Collections.sort(meusgatos, new ComparatorNomeCorIdade()) ou meusGatos.sort(new ComparadorCor());


### Stream API
 - Classe anonima
 - Funcional interface
 - - Comparator
 - - Consumer
 - - Function
 - - Predicate
 - Lambda ->
 - reference method ::
 - 
