all: Makefile jing pdf web

jing: *.ptx 
	jjing main.ptx
#	jing /home/ecb5/.ptx/2.29.1/core/schema/pretext.rng main.ptx
#	jing /home/ecb5/.ptx/2.6.2/core/schema/pretext.rng main.ptx

latex: *.ptx Makefile
	/home/ecb5/.local/bin/pretext build latex

pdf: *.ptx Makefile
	/home/ecb5/.local/bin/pretext build print

web: *.ptx Makefile
	/home/ecb5/.local/bin/pretext build web

view: Makefile *.ptx
	/home/ecb5/.local/bin/pretext view web

pdfview:
	/usr/bin/evince /home/ecb5/Dropbox/Books/MyBooks/ASORA-SecondEdition/output/print/main.pdf

deploy: jing
	/home/ecb5/.local/bin/pretext deploy -u
#	/home/ecb5/.local/bin/pretext view

LocalDeploy: *.ptx  Makefile
	scp -r /home/ecb5/Dropbox/Books/MyBooks/ASORA-SecondEdition/output/web/* leto:/var/www/html/ASORA
	# scp -r /home/ecb5/Dropbox/Books/MyBooks/ASORA-SecondEdition/output/web/knowl leto:/var/www/html/ASORA
	# scp -r /home/ecb5/Dropbox/Books/MyBooks/ASORA-SecondEdition/output/web/external leto:/var/www/html/ASORA
	# scp -r /home/ecb5/Dropbox/Books/MyBooks/ASORA-SecondEdition/output/web/_static leto:/var/www/html/ASORA

