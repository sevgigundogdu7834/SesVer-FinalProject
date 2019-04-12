# SesVer-FinalProject

Bu tez çalışmasında, konuşma ve duyma engellilere ve iletişimde bulundukları kişilere yönelik, örüntü tanıma tekniklerine dayalı Türkçe İşaret Dili Alfabesi Tanıma Sistemi geliştirilmiştir. Mevcut tanıma sistemlerinden farklı olarak, geliştirilen arayüz kullanılarak kullanıcı, kendi gösteriş tarzıyla alfabe işaretlerini gösterebilmekte ve kendine ait  veritabanını oluşturduktan sonra işaret tanıma aşamasına geçilmektedir. İşitme Engelli kişinin işaret dili ile söyledikleri metinsel olarak arayüze eklenir. Karşıdaki kişi ise  sesli olarak konuşması dinlenir ve yazıya dökülür.  (OpenCV Python SVM Classifier kullanılarak geliştirilen bir projedir.)

    k = 0xFF & cv2.waitKey(10)
    if k == 27:
        break
    if k == 13:
        name = str(i) + "_" + str(j) + ".jpg"
        cv2.imwrite(name, imgT)
        if (j < 20):
            j += 1
        else:
            while (0xFF & cv2.waitKey(0) != ord('n')):
                j = 1
            j = 1
            i += 1


       cap.release()
       cv2.destroyAllWindows()

•	El işaretlerini tespit etmek için YCBCR renk uzayını kullandık ve onlardan eğitim verilerini elde ettik.
•	Her harften 800 örnek oluşturularak 14.400 veri elde edilmiştir.

PyCharm programında yapmış olduğumuz tüm kod parçaları Tkinter GUI kullanılarak birleştirip bir arayüz oluşturulmuştur. Bu arayüzün iki fonksiyonu vardır. Biri işitme engelli kullanıcının işaretlerini alır ve yazıya döker diğeri ise gerçek zamanlı olarak iletişim kurmak istediği kişinin sesini dinler ve konuşma alanına yazar. ( Google Speech To Text)

    #import speech_recognition as sr


     def listen():

     r=sr.Recognizer()

     with sr.Microphone() as source:

      print('Say something')
      audio=r.listen(source)
      print('Done!')

     text=r.recognize_google(audio,language='tr-TR')

     print(text)

