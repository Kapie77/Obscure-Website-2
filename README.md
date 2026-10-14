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
```

# Como baixei os .swf do flash
```bash
cd /d "C:\Users\User\Music\obscure website (consertado)\pages\espanol\pages\bibliotheque"
mkdir swf
curl.exe -L "https://web.archive.org/web/20060102010046id_/http://es.obscure-game.com/bibliotheque_es.swf" -o "swf\bibliotheque_es.swf"
```

```bash
cd /d "C:\Users\User\Music\obscure website (consertado)\pages\espanol\pages\classroom"
mkdir swf
curl.exe -L "https://web.archive.org/web/20070108024927id_/http://es.obscure-game.com/classroom_es.swf" -o "swf\classroom_es.swf"
```
```bash
cd /d "C:\Users\User\Music\obscure website (consertado)\pages\espanol\pages\amphi"
mkdir swf
curl.exe -L "https://web.archive.org/web/20070112165355id_/http://es.obscure-game.com/amphitheatre_es.swf" -o "swf\amphitheatre_es.swf"
```

# Como arrumei os URLs dos .swf
Exemplo no do alemão:
(no index das pags):
../../de_index.htm
../amphi/amphi_de.htm
../classroom/classroom_de.htm
../bibliotheque/bibliotheque_de.htm

(no index principal dos idiomas):
pages/bibliotheque/bibliotheque_de.htm
pages/amphi/amphi_de.htm
pages/clasroom/classroom_de.htm

patch:
./files/Obscure_1_1_Patch_UK.exe

./files/Obscure_1_1_Patch_SP_DE.exe

./files/Obscure_1_1_Patch_FR_IT.exe

../../files/bande_annonce.zip
