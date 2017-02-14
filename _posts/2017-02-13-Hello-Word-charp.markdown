---
layout: post
title: Iniciando no c#
date: 2017-02-13 21:30:00 +0200
categoria: c# iniciante
---
Ei leitor, seja muito bem vindo ao meu blog. Este é o meu primeiro post e estou trazendo para você um conteúdo bem bacana sobre c#, para você quer iniciar nessa linguagem mas precisa de um empurrãozinho.

Nesse tutorial estarei utilizando duas ferramentas de software livre, pois acredito que todos devem ter a oportunidade de programar não importando o sistema operacional e que sejam instalações simples e limpa. Estarei utilizando o [visual studio code](https://code.visualstudio.com/){:target="_blank"} que é um editor de texto que faz parte de uma iniciativa open source da Microsoft e em conjunto vou utilizar o [.net core](https://www.microsoft.com/net/core){:target="_blank"}. Porém, se quiserem utilizar outras ferramentas como a IDE visual studio fique a vontade.

Sem mais delongas e com todas as ferramentas prontas, criaremos um projeto .net core console. Para isso crie um diretório em sistema, em seguida abra o terminal ou cmd se estiver no windows e digite os seguintes comandos e em seguida aperte enter:

~~~
> $dotnet new -t console
Created new C# project in /home/haruno/Documentos/Iniciante/Hello World.

> $dotnet restore
log  : Restore completed in 1632ms.
~~~

Agora abra o visual studio code, no menu global clique em [Arquivos >> Abrir pasta] e selecione a pasta que criou o novo projeto. Ele já criou para nós um projetinho console com hello word feito, mas não vamos usar esse, vamos fazer um porque o que queremos é aprender, certo? Apague tudo o que estiver escrito no arquivo. Em seguida insere o seguinte código:

~~~
class HelloWord
{

}
~~~

Csharp é uma linguagem orientada a objetos, usa outros paradigmas também, porém esse é muito visível, se não souber o que é orientação a objetos ou paradigmas não se preocupe, não fará diferença aqui. Tudo no c# precisa estar dentro de uma classe por isso criamos uma chamada 'HelloWord'. No c# é comum usar '{' e '}' para definição de escopos, mas vamos deixar isso para uma outra hora. Bem, como toda aplicação nativa, precisa-se ter um método 'main', então vamos criar:

~~~
class HelloWord
{
    public static void Main()
    {
        System.Console.WriteLine("Hello World!");
    }
}
~~~

Se não entender tudo o que está escrito não se preocupe, uma coisa de cada vez. No c# o final da linha do comando é finalizando com um '**;**' caso apareça um erro como : ***error CS1002: ; expected*** é porque esqueceu de colocar um **;** ao final de algum comando.
Abra o terminal novamente, use o atalho [ **ctrl + shift + ' ** ] para abrir o navegador no vs code e em seguida execute o seguinte comando:

~~~
> $dotnet build
Project Hello World (.NETCoreApp,Version=v1.1) will be compiled because expected outputs are missing
Compiling Hello World for .NETCoreApp,Version=v1.1

Compilation succeeded.
    0 Warning(s)
    0 Error(s)

Time elapsed 00:00:01.7908239
~~~

Com isso a nossa aplicação foi construída, agora é só rodar:

~~~
> $dotnet run
Project Hello World (.NETCoreApp,Version=v1.1) was previously compiled. Skipping compilation.
Hello World!
~~~

Muito legal não é mesmo, agora vamos fazer um algorítimo que lê um nome e aprensente uma mensagem de boas vindas ao csharp

~~~
class HelloWord{
    public static void Main(){
        System.Console.WriteLine("Digite o seu nome:");
        var nome = System.Console.ReadLine();
        System.Console.WriteLine($"Seja muito bem vindo ao csharp {nome}, espero que goste da experiência!");
    }
}
~~~

Agora é só rodar o projeto e ficará assim:

~~~
> $dotnet run

Project Hello World (.NETCoreApp,Version=v1.1) will be compiled because inputs were modified
Compiling Hello World for .NETCoreApp,Version=v1.1

Compilation succeeded.
    0 Warning(s)
    0 Error(s)

Time elapsed 00:00:01.7883339

Digite o seu nome:

> Haruno Kenobi
Seja muito bem vindo ao csharp Haruno Kenobi, espero que goste da experiência!
~~~

Agora teste, mude textos e entradas de textos e divirta-se, por enquanto é só e logo mais eu estarei trazendo a seguência do conteúdo.
O fonte dessa aplicação ficará no meu [Github](https://github.com/HarunoKenobi/csharp_beginning/tree/master/Hello%20World) acesse e dê um fork na aplicação e qualquer dúvida ou feed back poste nas [Issues](https://github.com/HarunoKenobi/csharp_beginning/issues).