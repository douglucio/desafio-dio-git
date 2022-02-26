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
 - No arquivo digite o seguinte código:
 -- //Minha Primeira Classe Java
 -- Class OlaMundo {               
 -- public static void main(String[] args) {  
 -- System.out.println(“Hello, Word Java!!!!”); 
 -- }
 -- }
 - No cmd digite javac OlaMundo.java 
 - O comando anterior vai criar o arquivo OlaMundo.class
 - No cmd digite java OlaMundo
 - No cmd será escrito a mensagem Hello, Word Java!!!!

### Instalando IDE Eclipse
 - Acesse https://www.eclipse.org/downloads/
 - 
