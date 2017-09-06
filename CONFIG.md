
# Test du BlurAdmin Angular admin panel front-end framework

Voici quelques erreurs rencontrées lors de l'installation et le paramétrage...
## npm install
retourne
[        ..........] - fetchMetadata: sill fetchPackageMetaData Error: unable to verify the first certificate

## npm config set registry

A la suite d'erreur de config et d'erreur de certificat :
Passons les commandes :
>npm config set registry http://registry.npmjs.org/

des ERR apparaissent conseillant de remettre à vide 
>npm config set registry   

(notemment sur tar2.xx.gz)
(Pb de firewall !! Barakuda)

>npm install

puis

>gulp serve



