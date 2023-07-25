# :white_check_mark: Workshop5 - Voice of Customer Analytics
## Objective
Topic modeling for hotel review.
The hotel that we would like to understand customer voice is [Scent of Sukhothai Resort](https://www.agoda.com/th-th/scent-of-sukhothai-resort/reviews/sukhothai-th.html?finalPriceView=1&isShowMobileAppPrice=false&cid=1844104&numberOfBedrooms=&familyMode=false&adults=2&children=0&rooms=1&maxRooms=0&checkIn=2023-08-1&isCalendarCallout=false&childAges=&numberOfGuest=0&missingChildAges=false&travellerType=1&showReviewSubmissionEntry=false&currencyCode=THB&isFreeOccSearch=false&isCityHaveAsq=false&los=1&searchrequestid=d20a9cff-bc06-454b-a07e-ba39b8578414) by extecting the 50 latest reviews.

### Notebook: [VoiceOfCustomer](https://github.com/Thaniparn/MADT8101-Customer-Analytics/blob/b7ba4288f7247bfd8e40c964467c9eed05e5025a/Workshop5%20-%20Voice%20of%20Customer%20Analytics/VoiceOfCustomer.ipynb)
### Google Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Thaniparn/MADT8101-Customer-Analytics/blob/main/Workshop5%20-%20Voice%20of%20Customer%20Analytics/VoiceOfCustomer.ipynb)

## Data Preparation
1. Get customer review into dataframe by using web scraping

![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/04084b97-c788-4569-a1ee-34534f1442da)

2. Remove stop word and useless word for analysis.
```python 
stopwords = list(pythainlp.corpus.thai_stopwords())
removed_words = [' ','  ','\n','(',')','สุโขทัย','รร','โรงแรม','ค่ะ','คะ','ๆ','มี','และ','รร.','ลูกค้า','ๆๆ','ค่','-','ประวัติศาสตร์']
screening_words = stopwords + removed_words

existing_words = set(thai_words())
#add_dict = {'อุทยานประวัติศาสตร์':'อุทยานประวัติศาสตร์','อุทยานประวัติศาสตร์สุโขทัย':'อุทยานประวัติศาสตร์','ราคา': 'ราคา','ปาท่องโก๋': 'ปาท่องโก๋','คุ้มค่า':'คุ้มค่า','สงบ':'สงบ','สไสตล์':'สไตล์','มากกก':'มาก','ไม่มี':'ไม่มี','รถส่วนตัว':'รถส่วนตัว','แหล่งท่งเที่ยว':'แหล่งท่องเที่ยว','สะพานบุญ':'สะพานบุญ','ไม่ได้':'ไม่ได้','อีกรอบ':'อีกรอบ'}
words = {'อุทยาน','ราคา','ปาท่องโก๋','คุ้มค่า','สงบ','สไสตส์','มากกก','ไม่มี','รถส่วนตัว','แหล่งท่งเที่ยว','สะพานบุญ','ไม่ได้','อีกรอบ','เหใาะสม','อพำนวย','สงบดี','ราคาที่'}
custom_dict = existing_words.union(words)

custom_dictionary_trie = Trie(custom_dict)
```
3. Token sentence to word with comma
```python 
def tokenize_with_comma(sentence):
  merged = ''
  words = pythainlp.word_tokenize(str(sentence), engine = 'newmm',custom_dict = custom_dictionary_trie)
  print(words)
  for word in words:
    if word not in screening_words:
      merged = merged + ',' + word
  return merged[1:]
```
## Topic Modeling
Create dictionary and do topic modeling. After randomly running in multiple topic, we use 3 models due to less overlap and show understanding model.
Your recently running result might not be the same with mine.
Here is my result
### Model 1: Overall Environment

![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/80a3c3cd-314e-4fc5-a4ee-28f1cbaaaaa2)

### Model 2: Cleanliness
![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/721af491-cc2b-4b3b-aefb-22cd7857b302)


### Model 3: Value for money
![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/f67714a7-582b-44d2-8602-91da521f597e)

## Word cloud
![image](https://github.com/Thaniparn/MADT8101-Customer-Analytics/assets/137845227/3abaca5a-b443-44ce-bae5-02ed4c400b71)
