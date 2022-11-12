# Yorumlar-ile-Duygu-Analizi
![](https://teknoloji.org/wp-content/uploads/2020/06/sentiment_analysis.png)

Merhaba, TechCareer tarafından düzenlenen Machine Learning Bootcamp eğitiminin son aşaması olan bu projemi sizlere tanıtmak istiyorum. İlk önce eğitimden bahsedelim, Machine Learning Bootcamp sürecinde, makine öğrenimi modelleri ve derin öğrenme modelleri üzerinde eğitim geçekleştirdik. Bu eğitim 1 ay'lık bir zaman diliminde gerçekleşmiştir. Şimdi projemden bahsetmem gerekir ise, ben bu projemde ürün yorumlarından oluşan veri setinden yorumları sınıflandırma işlemi gerçekleştirdim. Projem boyunca uyguladığım Makine öğrenimi modelleri:

- Naive Bayes Classification
  - Gaussian Naive Bayes
  - Multinomial Naive Bayes
  - Bernoulli Naive Bayes
- Support Vector Machine Classification
- Logistic Regression
- K-Nearest Neighbors(KNN)
- Decision Tree Classification
- Random Forest Classification<br>
Uyguladığım makine öğrenimi modellerini eğitim sonuçlarını karşılaştırdım. Aynı zamanda derin öğrenme modelleri olan RNN(Reccurrent Neural Network) ve LSTM(Long short-term memory) modellerini uyguladım. Umarım projem sizin için yararlı olmuştur.

[Projeyi Kaggle web sitesinde geliştirdim buraya tıklayarak Kaggle'da inceleye bilirsiniz!](https://www.kaggle.com/code/ihsncnkz/techcareer-project)

Proje sonuçlarının değerlendirilmesi:<br>

Projemde kullandığım makine öğrenimi modellerimi üç aşamada eğitim gerçekleştirdim ve sonuçlarını kaydettim. Bu aşamalarımın ilki 500 kelime darcığına sahip olan veri setim ile gerçekleştirildi. İkinci aşama 1000 kelime darcığına sahip veri seti ile gerçekleştirildi. Üçüncü aşama 2000 kelime darcığı ile gerçekleştirildi.<br>

Eğitimler boyunca test ve train veri setleri ile birlilte modellin skorlarımı hesaplmadım ve model sonucumu hesaplarken accurucy ve Cross validation sonuçlarını inceledim.<br>

**1. Naive Baye Classification**<br>
  **a. Gaussian Naive Bayes**
 
  | Kelime Darcığı	| Gaussian Accuracy	| Gaussian Test Score	| Gaussian Train Score	| Gaussian Cross Validation Mean	| Gaussian Cross Validation Std|
  | ------- | ------- | ------- | ------- | ------- | ------- |
  | 500	  | 0.5974798739936997	| 0.5974798739936997	| 0.6259773602520714   | 0.5997183321174273	| 0.011104129720831383 |
  | 1000	| 0.5698284914245713	| 0.5698284914245713	| 0.623059866962306	   | 0.5740454796562221	| 0.008051221125886736 |
  | 2000	| 0.5456772838641932	| 0.5456772838641932	| 0.6286614540786556	 | 0.5406695044620689	| 0.003189285110471602 |
	
  **b. Bernoulli Naive Bayes**
  
  | Kelime Darcığı	| Bernoulli Accuracy	| Bernoulli Test Score	| Bernoulli Train Score	| Bernoulli Cross Validation Mean	| Bernoulli Cross Validation Std|
  | ------- | ------- | ------- | ------- | ------- | ------- |
  | 500	  | 0.6604830241512075	| 0.6604830241512075	| 0.6874781188003267   | 0.6696225105429617	| 0.004896071672541835 |
  | 1000	| 0.6604830241512075	| 0.6604830241512075	| 0.7021822849807445   | 0.6719567096559291	| 0.005046355613186887 |
  | 2000	| 0.6625831291564578	| 0.6625831291564578	| 0.7142023573345782	 | 0.6653052605479003	| 0.006539737096117522 |
  
  **c. Multinomial Naive Bayes**
  
  | Kelime Darcığı	| Multinomial Accuracy	| Multinomial Test Score	| Multinomial Train Score	| Multinomial Cross Validation Mean	| Multinomial Cross Validation Std|
  | ------- | ------- | ------- | ------- | ------- | ------- |
  | 500	  | 0.6772838641932096	| 0.6772838641932096	| 0.7060333761232349   | 0.6829260218209164	| 0.006244618594406014 |
  | 1000	| 0.6870843542177109	| 0.6870843542177109	| 0.7331077138522581   | 0.701948787533863	| 0.004299917405953132 |
  | 2000	| 0.6972348617430871	| 0.6972348617430871	| 0.7620492472867313	 | 0.7109342314008942	| 0.005433942546477297 |
  
**2. Support Vector Machine Classification**<br>
  **a. SVC with Kernel: "rbf"**
  
  | Kelime Darcığı	| Rbf ile SVC Accuracy	| Rbf ile SVC Test Score	| Rbf ile SVC Train Score	| Rbf ile SVC Cross Validation Mean	| Rbf ile SVC Cross Validation Std|
  | ------- | ------- | ------- | ------- | ------- | ------- |
  | 500	  | 0.6737836891844592	| 0.6737836891844592	| 0.839887968257673   | 0.6800079834282557	| 0.005870865454986121 |
  | 1000	| 0.680434021701085	| 0.680434021701085	| 0.8593768234333061   | 0.6864268777234424	| 0.004711228897644023 |
  | 2000	| 0.6853342667133356	| 0.6853342667133356	| 0.8695297000816898	 | 0.6870105807671585	| 0.004207592051120965 |
  
  **b. SVC with Kernal: "linear"**
  
  | Kelime Darcığı	| linear ile SVC Accuracy	| linear ile SVC Test Score	| linear ile SVC Train Score	| linear ile SVC Cross Validation Mean	| linear ile SVC Cross Validation Std|
  | ------- | ------- | ------- | ------- | ------- | ------- |
  | 500	  | 0.6737836891844592	| 0.6695834791739587	| 0.755747461780838   | 0.6800079834282557	| 0.005870865454986121 |
  | 1000	| 0.680434021701085| 0.672033601680084	| 0.8116466332127437  | 0.6864268777234424	| 0.004711228897644023 |
  | 2000	| 0.6853342667133356	| 0.6762338116905845	| 0.8759481853191737	 | 0.6870105807671585	| 0.004207592051120965 |
  
  **c. SVC with Kernal: "poly"**
  
  | Kelime Darcığı	| poly ile SVC Accuracy	| poly ile SVC Test Score	| poly ile SVC Train Score	| poly ile SVC Cross Validation Mean	| poly ile SVC Cross Validation Std|
  | ------- | ------- | ------- | ------- | ------- | ------- |
  | 500	  | 0.6737836891844592	| 0.6051802590129507 | 0.7790874080989614  | 0.6113889870923224	| 0.005622960807026126 |
  | 1000	| 0.680434021701085 | 0.6209310465523277	| 0.8000933597852725  | 0.6354295281943759	| 0.006230545083575114 |
  | 2000	| 0.6853342667133356	| 0.5848792439621981	| 0.7839887968257673	 | 0.5522199993051965	| 0.024281738731952416 |
  
  **d. SVC with Kernal: "sigmoid"**
  
  | Kelime Darcığı	| sigmoid ile SVC Accuracy	| sigmoid ile SVC Test Score	| sigmoid ile SVC Train Score	| sigmoid ile SVC Cross Validation Mean	| sigmoid ile SVC Cross Validation Std|
  | ------- | ------- | ------- | ------- | ------- | ------- |
  | 500	  | 0.6737836891844592	| 0.5656282814140707 | 0.5968024273544171  | 0.5902689366305165	| 0.010805304981772162 |
  | 1000	| 0.680434021701085 | 0.5831291564578229	| 0.6277278562259306 | 0.6141910886685045	| 0.009615727301946037 |
  | 2000	| 0.6853342667133356	| 0.5950297514875744	| 0.6487338079122418	| 0.6292455047236419	| 0.010780552896806215 |
  
**3. Logistic Regression**

  | Kelime Darcığı	| Logistic Regression Accuracy	| Logistic Regression Test Score	| Logistic Regression Train Score	| Logistic Regression Cross Validation Mean	| Logistic Regression Cross Validation Std|
  | ------- | ------- | ------- | ------- | ------- | ------- |
  | 500	  | 0.6772838641932096	| 0.6772838641932096 | 0.7420935931847357  | 0.6496420246420246	| 0.01686411863047354 |
  | 1000	| 0.6807840392019601| 0.6807840392019601	| 0.7933247753530167 | 0.6538441950206657	| 0.020209533776940854 |
  | 2000	| 0.6818340917045852	| 0.6818340917045852	| 0.8590267242385342	| 0.6594405594405595	| 0.016943854683223097 |
  
Bundan sonraki modellerimde GridSearch modeli ile birlilte uyguladım!<br>

**4. K-Nearest Neighbors(KNN)**

Max_Feature: 500

GridSearch ile knn modelinin en iyi parametırları:  {'n_neighbors': 9, 'p': 1, 'weights': 'distance'}

GridSearch ile knn modelinin en iyi skoru:  0.5727618703415415

-------------------------------------------------------------------------------------------------------

Max_Feature: 1000

GridSearch ile knn modelinin en iyi parametırları:  {'n_neighbors': 8, 'p': 1, 'weights': 'distance'}

GridSearch ile knn modelinin en iyi skoru:  0.5673950712654015

-------------------------------------------------------------------------------------------------------

Max_Feature: 2000

GridSearch ile knn modelinin en iyi parametırları:  {'n_neighbors': 3, 'p': 1, 'weights': 'distance'}

GridSearch ile knn modelinin en iyi skoru:  0.5612109519496086

-------------------------------------------------------------------------------------------------------
  
**5. Decision Tree Classification**

Max_Feature: 500

GridSearch ile dtc modelinin en iyi parametırları: {'criterion': 'gini', 'splitter': 'random'}

GridSearch ile dtc modelinin en iyi skoru:  0.5703108354867845

-------------------------------------------------------------------------------------------------------

Max_Feature: 1000

GridSearch ile dtc modelinin en iyi parametırları: {'criterion': 'entropy', 'splitter': 'random'}

GridSearch ile dtc modelinin en iyi skoru:  0.5810478647828707

-------------------------------------------------------------------------------------------------------

Max_Feature: 2000

GridSearch ile dtc modelinin en iyi parametırları: {'criterion': 'entropy', 'splitter': 'best'}

GridSearch ile dtc modelinin en iyi skoru:  0.584198417273271
  
-------------------------------------------------------------------------------------------------------

**6. Random Forest Classification**

Max_Feature: 500

GridSearch ile rfc modelinin en iyi parametırları: {'class_weight': 'balanced', 'criterion': 'entropy', 'n_estimators': 7}

GridSearch ile rfc modelinin en iyi skoru:  0.6351956710511238

-------------------------------------------------------------------------------------------------------

Max_Feature: 1000

GridSearch ile rfc modelinin en iyi parametırları: {'class_weight': 'balanced', 'criterion': 'gini', 'n_estimators': 9}

GridSearch ile rfc modelinin en iyi skoru:  0.6409145163742896

-------------------------------------------------------------------------------------------------------

Max_Feature: 2000

GridSearch ile rfc modelinin en iyi parametırları: {'class_weight': 'balanced', 'criterion': 'entropy', 'n_estimators': 9}

GridSearch ile rfc modelinin en iyi skoru:  0.638697670699949
  
-------------------------------------------------------------------------------------------------------
  
Projemin en son 2000 kelime darcığı ile en son eğitimi jupiter notebook olarak yukarıdaki dosyadan inceleye bilirsiniz!
  
TechCareer ailese böylesine güzel bir makine öğrenimi bootcamp'i düzenledikleri için teşekkür ederim sizlerde TechCareer'in eğitimlerine katılmak isterseniz aşağıda linkleri paylaşıyor olacağım!

**Linkler**<br>
TechCareer web sitesine ulaşmak için aşağıdaki resme tıklaya bilirsiniz!<br>
[![](https://www.kariyer.net/kariyer-rehberi/wp-content/uploads/2021/05/logo.png)](https://www.techcareer.net/)

**Sosyal meyda hesaplarım:**<br>
[LinledIn](https://www.linkedin.com/in/ihsan-cenk%C4%B1z-b070a7154/)
[Kaggle](https://www.kaggle.com/ihsncnkz)
  
  
