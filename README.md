# local-nuget-package

Criando um package nuget (repositório local)<br />
.NET Standard

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

<br/><br/><br/>

.NET Framework 4<br/>

1. Para criar um pacote com framework 4.0 ou superior, você vai precisar baixar o nuget.exe<br />
https://www.nuget.org/downloads

2. Crie um arquvivo .nuspec e informe os dados do package que deseja criar<br/>
![nuspec](https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/nuspec.jpg)
<br/>

```
<?xml version="1.0" encoding="utf-8"?>
<package >
  <metadata>
    <id>Package</id>
    <version>1.0.0</version>
    <authors>Raywall Malheiros</authors>
    <requireLicenseAcceptance>false</requireLicenseAcceptance>
    <license type="expression">MIT</license>
    <projectUrl>https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/pack.jpg</projectUrl>
    <iconUrl>https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/pack.jpg</iconUrl>
    <description>Teste de geração de pacote</description>
    <releaseNotes>Teste de criação de pacote</releaseNotes>
    <copyright>Copyright 2020</copyright>
    <tags>teste pacote framework nuget</tags>
    <dependencies>
      <group targetFramework=".NETFramework4.0">
        <dependency id="Newtonsoft.Json" version="12.0.3" />
      </group>
    </dependencies>
  </metadata>
  <files>
    <file src="C:\Users\raywa\Source\Repos\local-nuget-package\local-nuget-framework-package\bin\Debug\*.dll" />
  </files>
</package>
```

3. Para gerar o pacote, utilize o nuget.exe<br/>
```
nuget pack [caminho do arquivo nuspec]
```
<br/>
![command](https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/command.jpg)

4. Pronto! Seu package está pronto para ser adicionado ao repositorio!

<br/><br/><br/>

Para inserir a referencia do package em um projeto:<br/>

1. Abra o gerenciamento de pacotes nuget:<br/>
![manager nuget package](https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/manage-nuget-packages.jpg)

2. Adicione o repositório local:<br/>
![novo repositorio](https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/repositorio-local.jpg)

3. Pronto! Agora você já pode pesquisar e incluir o repositório ao seu projeto.<br/>
![search](https://github.com/raywall/local-nuget-package/blob/master/local-nuget-package/images/consulta.jpg)
<br /><br />


