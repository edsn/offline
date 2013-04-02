## ����

Offline��һ�����ߴ洢������Ƕ�gallery����֮ǰһ�����ߴ洢��local-storage���ĸĽ���

* �汾��1.0
* ���ڣ�kissy1.20���߸��߰汾
* ���ߣ�����


#### Offline������

* ��localStorage�͵Ͱ汾��ie userData����������ֱ�����ļ�
* �ṩ�˹���ʱ�䴦��
* ���û�������ӣ�ɾ���Ȳ�����ʱ���ṩ�¼������������û�����
* ÿ���ⲿ�������ṩ�˷���ֵ������д��Ԫ����
* ��ÿ������Ĳ�������������֤
* �ṩ��ͳ��ʹ���ֽڵķ����������û�����ʣ������

## demo

[�������](http://sirzxj.github.com/gallery/offline/1.0/demo.html)

## ���ʹ��

kissy1.2����Ҫgallery�İ����ã�

```javascript
KISSY.config({
    packages:[
        {
            name:"gallery",
            path:"http://a.tbcdn.cn/s/kissy/",
            charset:"utf-8"
        }
    ]
});
```

kissy1.3�Ͳ���Ҫ�����á�




### 1.����Offlineģ��,��ʼ��Offline

```javascript
    KISSY.use('gallery/offline/1.0/index', function (S, Offline) {
        var offline = new Offline();
    })
```
**����**��use()�Ļص�����һ��������KISSY���ڶ����������������

### 2. ʹ��setItem������������
offline.setItem(key, value, deadline);
**����**��key��value���붼���ַ���,����������deadline�ǿ�ѡ�ģ���λΪ���룬����key�Ĺ���ʱ�䣬���ں��Զ����key
	

```javascript
//��key1 �浽�������30��
offline.setItem('key1','value1',1000*60*60*24*30);
```
����ֵ���ɹ�����true,ʧ�ܷ���false



### 3. ���淽��
getItem���,removeItem�Ƴ���clear���

### 4. ��������	

* timeRemain
	��ȡĳ��key�洢��ʣ��ʱ�䣨��������,û�����Ƶ�key�᷵��-1
* size
	��ȡ���ش洢���ֶ���
* getAll
	��ȡȫ���洢���ֶ�
	**����**��getAllĬ�Ϸ��ص�������key��value ���� stringify ���ַ�����������true����ʱ���򷵻ض���
* usedByte
	����������б��ش洢�Ѿ�ʹ�õ��ֽ�����

### 5. ����
��ʹ��setItem,removeItem,clear��ʱ�򣬷ֱ�ΪΪKISSY.Offline ������ setItem��removeItem,clear���¼������ڼ���	 

