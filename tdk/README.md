# TDK - Scientific Student Competition

## English Absrtact

`Enhancing Sign Language Translation with Graph Neural Networks for Hand Pose Classification and Fingerspelling Sequence Translation`

Despite advancements in natural language processing and sign language recognition technologies, effective translation solutions for the deaf and hard of hearing community, comprising approximately 1.5 billion individuals globally, remain elusive. Previous work explored pose approximation algorithms and conventional neural network architectures to improve translation accuracy. However, the complex dynamics of hand movements, with joints influencing one another, continue to pose a unique challenge.

Initially, individual hand poses were classified using traditional methods, such as multilayer perceptron-based approaches. In this follow-up research, I propose classifying the same poses using Graph Neural Networks (GNNs), specifically the GCN and GAT architectures, to model the hand as a graph where each joint acts as a node and the connections between them represent joint dependencies. For translating fingerspelling sequences—previously relying on a transformer architecture with a convolution-based embedding layer for pose sequences—I now introduce a custom graph-based embedding layer. This layer is designed to capture the relational structure of hand movements more effectively while still utilizing the transformer model for sequential data processing.

This research aims to validate the hypothesis that GNNs can outperform traditional methods under specific conditions, such as complex sign language poses where joints are obscured or highly dependent on one another. To test this hypothesis, I will design and implement several GNN architectures, followed by comprehensive experiments to measure their performance. Metrics such as translation accuracy and processing speed will be compared against prior models.

Additionally, I will explore the practical usability of this approach in real-time applications, considering challenges like computational efficiency and scalability across diverse sign language dialects. By examining the conditions under which GNNs can enhance translation, this research seeks to provide insights into the future of accessible, high-quality sign language interpretation systems. Ultimately, the goal is to refine and improve current sign language translation technologies, making them more reliable and adaptable to real-world scenarios.

## Magyar Absztrakt

`Jelnyelvfordítás Javítása Gráf Neurális Hálózatokkal: Kézjelek Osztályozása és Ujj Betűzés Fordítása`

Annak ellenére, hogy a természetes nyelvfeldolgozás és a jelnyelvfelismerés terén jelentős előrelépések történtek, a nagyjából 1,5 milliárd fős siket és nagyothalló közösség számára továbbra is hiányoznak a hatékony fordítási megoldások. Korábbi munkám pózbecslési algoritmusok és hagyományos neurális hálózati architektúrák alkalmazását vizsgálták Azonban a kézmozgások összetett dinamikája, ahol az ízületek hatással vannak egymásra, különleges kihívást jelent.

Kezdetben az egyes kézpózokat hagyományos módszerekkel, például MLP alapú megközelítésekkel osztályoztam. Ebben a folytatólagos kutatásban, ugyanezeket a pózokat gráf neurális hálózatokkal, azon belül: GCN és GAT architektúrák alkalmazásával osztályozom, ahol a kéz ízületeit csomópontokként modellezem, az ezek közötti kapcsolatok pedig az ízületek közötti függőségeket tükrözik. Az ujj betűzés fordításához, amely korábban transzformer architektúrát használt egy konvolúció alapú “embedding” réteggel a póz sorozatokhoz, most egy egyedi gráf alapú embedding réteget tervezek. Ez várhatóan hatékonyabban képes megragadni a kézmozdulatok relációs szerkezetét, miközben továbbra is kihasználja a transzformer modellt a szekvenciális adatok feldolgozásához.

A kutatás célja annak a hipotézisnek az igazolása, hogy a GNN-ek bizonyos körülmények között, például bonyolult jelnyelvi pózok esetén, ahol az ízületek erősen függenek egymástól, felülmúlhatják a hagyományos módszereket. Ennek teszteléséhez először több GNN architektúrát valósítok meg, majd átfogó kísérleteket végzek azok teljesítményének mérésére. A fordítás pontosságát és a feldolgozási sebességet a korábbi modellekkel hasonlítom össze.

Emellett megvizsgálom az új megközelítés gyakorlati használhatóságát valós idejű alkalmazásokban, figyelembe véve a számítási hatékonyságot és a különböző jelnyelvi dialektusok közötti skálázhatóságot. A GNN-ek fordítási teljesítményének vizsgálatával, a kutatás célja, hogy betekintést nyújtson a hozzáférhető, magas minőségű jelnyelvfordító rendszerek jövőjébe.
