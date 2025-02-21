# MobaXterm Keygen

## How it work?

Please see source code. It is not complex.

## How to use?

```
Usage:
    MobaXterm-Keygen.py <UserName> <Version>

    <UserName>:      The Name licensed to
    <Version>:       The Version of MobaXterm
                     Example:    10.9
```

EXAMPLE:

```
PS C:\Users\DoubleSine\Github\MobaXterm-Keygen> .\MobaXterm-Keygen.py "DoubleSine" 10.9
[*] Success!
[*] File generated: C:\Users\DoubleSine\Github\MobaXterm-Keygen\Custom.mxtpro
[*] Please move or copy the newly-generated file to MobaXterm's installation path.
```
Then copy `Custom.mxtpro` to `C:\Program Files (x86)\Mobatek\MobaXterm`.

## For Portable version using WSL to generate
```
mkdir /mnt/c/Users/<UserName>/Documents/My-MobaXTerm
curl -LO https://download.mobatek.net/2152021112100754/MobaXterm_Portable_v21.5.zip
unzip MobaXterm_Portable_v21.5.zip
git clone https://github.com/flygon2018/MobaXterm-keygen.git
cd MobaXterm-keygen/
python3 MobaXterm-Keygen.py <UserName> <Version>
mv Custom.mxtpro ../
cd ../
echo '[Misc]
HomeDir="C:\Users\UserName\Documents\My-MobaXTerm"' > MobaXterm.ini
Launch MobaXterm_Personal_[version number].exe
```

## Screenshot

![](pic0.png)

## Postscript

1. This application does not have complex activation algorithm and it is truly fantastic. __So please pay for it if possible.__

2. The file generated, `Custom.mxtpro`, is actually a zip file and contains a text file, `Pro.key`, where there is a key string. 

3. `MobaXterm.exe` has another mode. You can see it by adding a parameter `"-customizer"`.

   ```
   $ .\MobaXterm.exe -customizer
   ```

   I don't know how to make custom settings take effect in `Customizer` mode directly. 
   
   The only way I found is that you should export custom settings to a file named `MobaXterm customization.custom` which is also a zip file. Then merge two zip file: `Custom.mxtpro` and `MobaXterm customization.custom` to `Custom.mxtpro`. Finally copy newly-generated `Custom.mxtpro` to MobaXterm's installation path.

