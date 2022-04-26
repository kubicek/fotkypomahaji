# jekyll based website

## generating thumbnails

    ```
    mogrify -path thumbs -resize 560x originals/* 
    mogrify -path images -resize 2048x originals/*
    ```


https://docs.google.com/forms/d/e/1FAIpQLSex-V5EJ5vHKFcF9f1pG-nPcKo2SgbuQdmAxnf0lZwOcMrzTg/viewform?usp=pp_url&entry.1896224007=Petr+Josek+1

https://docs.google.com/forms/d/e/1FAIpQLSex-V5EJ5vHKFcF9f1pG-nPcKo2SgbuQdmAxnf0lZwOcMrzTg/viewform?usp=pp_url&entry.1896224007=Petr+Josek+1&entry.1841723669=Ji%C5%99%C3%AD+Kub%C3%AD%C4%8Dek&entry.174872576=Kamenick%C3%A1+26&entry.578242619=170+00+Praha+7&entry.743304950=%2B420603876520&entry.700148599=jiri@kubicek.cz


File.open("_data/photos.yml","w"){|f| f<<YAML.load(File.read "_data/photogs.yml").collect{|photog| photog["images"].collect{|image| {filename:image["filename"],description:image["description"],photog:photog["name"],related:(photog["images"]-[image]).collect{|photo| photo["filename"]}}}}.flatten.to_yaml}