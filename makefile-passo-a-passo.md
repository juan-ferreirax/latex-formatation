# Instruções pra criar o makefile

1. Adicionar ```\listfiles``` na primeira linha do nomedoarquivo.tex
2. No terminal rodar ```xelatex nomedoarquivo.tex```
3. Ver no nomedoarquivo.log na sessão \*File List\* os com final .cls e .sty  
    3.1 Adicionar no makefile o nome das classes .cls apenas se não for classes padrão  
    3.2 Adicionar no makefile o nome de todos os pacotes .sty  
4. Criar um arquivo com nome makefile
5. Adicionar no arquivo makefile os nomes dos pacotes encontrados no passo 3:
```
install:
    # Pacotes usados na construção do arquivo latex.tex
	sudo tlmgr install babel babel-portuges geometry keyval ifvtex iftex

build:
	xelatex latex.tex
```

6. Opcional, remover da primeira linha do nomedoarquivo.tex o \listfiles após a compilação