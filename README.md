O [site do obscure](https://web.archive.org/web/20051106024935/http://www.obscure-game.com/fr/index.htm) foi feito em Flash Player 6.

Ruffle emula o Flash nos navegadores modernos. Ele consegue executar muitos arquivos antigos, embora alguns recursos do Flash Player 6 possam não ser totalmente compatíveis.

precisa da versão "self-hosted" do Ruffle.

Para editar o .swf (onde fica o flash do site) usei o programa [JPEXS Free Flash Decompiler](https://github.com/jindrapetrik/jpexs-decompiler).
O script responsável pelos idiomas da pagina principal é scripts -> frame 71 - DoAction

Como alterei o url do .exe: abri o "decor_anim_uk.swf", entrei em DefineButton 2 (child: 244) -> BUTTONCONDACTION on(release). Ou vá em Tols -> Text search e pesquise por "http://www.obscure-game.com/patch/Obscure_1_1_Patch_UK.exe".

./files/Obscure_1_1_Patch_UK.exe

os urls de "classrom", "anphi", também estão nesse .swf. Pesquisei pelo url em "text search" também e alterei eles.

# Como abrir um servidor local para testar o flash
Ir para a pasta do site:
```bash
cd /d "C:\Users\User\Music\obscure website (consertado)"
```
Criar servidor python local:
```bash
python -m http.server 8000
```
Exemplo:
```bash
http://localhost:8000/pages/english/uk_index.htm
```bash
