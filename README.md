# local-nuget-package
Criando um package nuget (repositório local)

1. Crie um projeto .NET Standard class library para que possa ser compartilhado como um package:<br/>
![new project](https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/criar-projeto.jpg)

2. Em seguida, vamos criar um metodo em uma classe publica da biblioteca:<br/>
```C#
namespace local_nuget_package
{
    public class Teste
    {
        public static int Dobro(int valor) => valor * 2;
    }
}
```

3. Nas propriedades do projeto, clique em Package e preencha o formulário com os detalhes do pacote:<br/>
![config](https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/configuracao.JPG)

4. Após o preenchimento publique o pacote:<br/>
![pack](https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/pack.jpg)

5. Após gerar o pacote, copie para uma pasta local ou na rede a qual todos de sua equipe tenham acesso:<br/>
![pasta local](https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/package-folder.jpg)

****<br/>

Para inserir a referencia do package em um projeto:<br/>

1. Abra o gerenciamento de pacotes nuget:<br/>
![manager nuget package](https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/manage-nuget-packages.jpg)

2. Adicione o repositório local:<br/>
![novo repositorio](https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/repositorio-local.jpg)

3. Pronto! Agora você já pode pesquisar e incluir o repositório ao seu projeto.<br/>
![search](https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/consulta.jpg)
