db.books.insertMany([
  {
    title: "The Master and Margarita",
    description: "Роман советского писателя Михаила Булгакова, написанный в Советском Союзе в период с 1928 по 1940 год. Цензурированная версия с несколькими вырезанными редакцией главами была опубликована в журнале «Москва» в 1966–1967 годах, после смерти писателя в марте. 10 октября 1940 года, его вдова Елена Булгакова.",
    authors: "Mikhail Bulgakov"
  },
  {
    title: "War and Peace",
    description: "«Война и мир» — литературное произведение русского писателя Льва Толстого. Действие произведения происходит во время наполеоновских войн. В нем художественное повествование сочетается с главами, посвященными истории и философии. Ранняя версия публиковалась серийно, начиная с 1865 года, после чего вся книга была переписана и опубликована в 1869 году.",
    authors: "Leo Tolstoy"
  }
]);

db.books.find({ title: "The Master and Margarita" });

db.books.updateOne(
  { _id: ObjectId("1") },
  {
    $set: {
      description: "Действие романа происходит приблизительно в середине 30-х годов XX века и начинается в один из майских дней, когда два московских литератора — председатель правления МАССОЛИТа Михаил Александрович Берлиоз и поэт Иван Бездомный — во время прогулки на Патриарших прудах встречают незнакомца, похожего на иностранца. Он включается в разговор об Иисусе Христе, рассказывает о своём пребывании на балконе прокуратора Иудеи Понтия Пилата и предрекает, что Берлиозу отрежет голову «русская женщина, комсомолка». Литераторы не знают, что перед ними Воланд — загадочный и могущественный гость, прибывший в советскую столицу со своей свитой: Фаготом-Коровьевым, Азазелло, котом Бегемотом и служанкой Геллой.",
      authors: "Михаил Булгаков"
    }
  }
);
