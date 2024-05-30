# Dio - Desafio POO

Para resolver este desafio, vamos seguir os seguintes passos:

- Assistir ao vídeo e entender as funcionalidades do iPhone conforme o lançamento de 2007.
- Criar um diagrama UML para as funcionalidades do iPhone.
- Implementar as classes e interfaces em Java (opcional).

# 1 - Funcionalidades a Modelar
- Reprodutor Musical

Métodos: tocar(), pausar(), selecionarMusica(String musica)
Aparelho Telefônico

Métodos: ligar(String numero), atender(), iniciarCorreioVoz()
Navegador na Internet

Métodos: exibirPagina(String url), adicionarNovaAba(), atualizarPagina()

# 2 - Criar o Diagrama UML
Usaremos uma ferramenta UML para criar o diagrama das classes e interfaces. Vamos definir três interfaces principais: ReprodutorMusical, AparelhoTelefonico, e NavegadorInternet. 
Em seguida, criaremos uma classe iPhone que implementa essas interfaces.

# Aqui está o diagrama UML:

  classDiagram
    ReprodutorMusical <|-- iPhone
    AparelhoTelefonico <|-- iPhone
    NavegadorInternet <|-- iPhone

    class ReprodutorMusical {
        +tocar()
        +pausar()
        +selecionarMusica(String musica)
    }

    class AparelhoTelefonico {
        +ligar(String numero)
        +atender()
        +iniciarCorreioVoz()
    }

    class NavegadorInternet {
        +exibirPagina(String url)
        +adicionarNovaAba()
        +atualizarPagina()
    }

    class iPhone {
    }

# 3 - Implementação em Java (Opcional)

A seguir, a implementação das interfaces e da classe iPhone em Java:

- ReprodutorMusical.java

public interface ReprodutorMusical {
    void tocar();
    void pausar();
    void selecionarMusica(String musica);
}

- AparelhoTelefonico.java

public interface AparelhoTelefonico {
    void ligar(String numero);
    void atender();
    void iniciarCorreioVoz();
}

- NavegadorInternet.java

public interface NavegadorInternet {
    void exibirPagina(String url);
    void adicionarNovaAba();
    void atualizarPagina();
}

- iPhone.java
public class iPhone implements ReprodutorMusical, AparelhoTelefonico, NavegadorInternet

------------------------------------------------------------------------------------

    {
    @Override  
      public void tocar() {
          System.out.println("Tocando música...");
      }

    @Override  
        public void pausar() {
        System.out.println("Música pausada.");
      }

    @Override  
        public void selecionarMusica(String musica) {
       System.out.println("Música selecionada: " + musica);
      }

    @Override  
        public void ligar(String numero) {
        System.out.println("Ligando para: " + numero);
       }

    @Override    
      public void atender() {
        System.out.println("Atendendo chamada...");
      }

    @Override  
      public void iniciarCorreioVoz() {
        System.out.println("Iniciando correio de voz...");
      }

    @Override
      public void exibirPagina(String url) {
        System.out.println("Exibindo página: " + url);
      }

    @Override  
      public void adicionarNovaAba() {
        System.out.println("Nova aba adicionada.");
      }

    @Override  
       public void atualizarPagina() {
        System.out.println("Página atualizada.");
      }

        public static void main(String[] args) {
        iPhone meuIphone = new iPhone();
        meuIphone.tocar();
        meuIphone.ligar("123456789");
        meuIphone.exibirPagina("www.example.com");
      }
    }

- Com isso, você tem um diagrama UML e a implementação em Java das funcionalidades principais do iPhone!
