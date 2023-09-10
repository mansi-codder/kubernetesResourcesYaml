kubectl create secret generic \
<secret-name> --fom-literal=key=value

kubectl create secret generic \
app-secret  --fom-literal=DB_Host=mysql \
            --fom-literal=DB_User=root \
            --fom-literal=DB_Password=paswrd


 kubectl create secret generic 
 <secret-name> --fom-file=<path-to-file>

  kubectl create secret generic 
app-secret --fom-file=app_secret.properties


in secret , put things with bse64 encoded
echo [Convert]::ToBase64String([Text.Encoding]::Unicode.GetBytes('mysql''))
echo[Convert]::ToBase64String([Text.Encoding]::Unicode.GetBytes('root''))
echo [Convert]::ToBase64String([Text.Encoding]::Unicode.GetBytes('paswrd''))

echo -n 'bQB5AHMAcQBsAA==' | base64 --decode
echo -n 'cgBvAG8AdAA=' | base64 --decode
echo -n 'cABhAHMAdwByAGQA' | base64  --decode
