{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TSX Dosyası - React TypeScript Dosyası - .tsx dosyası nedir ve nasıl açılır?",
  "description":"TSX React TypeScript dosyası ve nasıl açılacağı hakkında bilgi edinin.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-tr-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## TSX dosyası nedir?

".tsx" dosya uzantısı genellikle **React** kodunu içeren TypeScript dosyalarıyla ilişkilendirilir. **TypeScript, dile statik yazmayı ekleyen bir JavaScript üst kümesidir** ve **React, kullanıcı arayüzleri oluşturmaya yönelik bir JavaScript kitaplığıdır**. Geliştiriciler, React ve TypeScript ile birlikte çalışırken, dosyalarının hem TypeScript hem de JSX (React'in JavaScript için sözdizimi uzantısı) içerdiğini belirtmek için genellikle ".tsx" uzantısını kullanırlar.

## TSX Dosya Örneği

TypeScript değişkenleriniz, işlev parametreleriniz ve daha fazlası için türleri tanımlamanıza olanak tanır. React bileşenlerinde kullanılan props, state ve diğer değişkenlerin türlerini belirten bir ".tsx" dosyasında TypeScript kodunu sıklıkla göreceksiniz.

''''
// Örnek: React bileşenindeki TypeScript kodu
arayüz MyComponentProps {
   isim: dize;
   yaş: sayı;
}
const MyComponent: React.FC<MyComponentProps> = ({ isim, yaş }) => {
   // Bileşen mantığı burada
   return <div>{name}, {age} yaşında.</div>;
};
''''

## JSX (React Söz Dizimi Uzantısı)

JSX, React tarafından önerilen JavaScript için bir sözdizimi uzantısıdır. XML/HTML'ye benzer ve kullanıcı arayüzünün nasıl görünmesi gerektiğini tanımlamak için kullanılır.

''''
// Örnek: React bileşenindeki JSX
const MyComponent: React.FC<MyComponentProps> = ({ isim, yaş }) => {
   return <div>{name}, {age} yaşında.</div>;
};
''''

".tsx" dosyası genellikle işlevsel bileşenleri veya sınıf bileşenlerini kullanan bir React bileşeninin tanımını içerir.

''''
// Örnek: Bir ".tsx" dosyasındaki bileşen tanımına tepki verin
const MyComponent: React.FC = () => {
   return <div>Merhaba, React!</div>;
};
''''

Genellikle dosyanın başında gerekli bağımlılıkları ve modülleri getiren import ifadelerini göreceksiniz.

''''
// Örnek: İfadeleri bir ".tsx" dosyasına aktarın
React'ı 'react'tan içe aktarın;
''''

## TSX dosyası nasıl açılır?

TSX dosyaları düz metin dosyaları olduğundan bunları herhangi bir metin düzenleyicide açabilirsiniz; Not defteri. Ancak bunlar kodlama dosyalarıdır ve IDE tarafından açılması gerekir; Visual Studio Kodu.