### lambda

lambda�Ƃ́A�����֐��i�����O���t���Ă��Ȃ��֐��j��\������L�@�̈�ł��B

��Ƃ���python����ŁAa,b�������Ƃ��Ď󂯎��A���̘a��Ԃ��֐����L�q���܂��B

	def fnuc(a,b):
	    return a+b

���̏ꍇ�A�֐��ɂ�func�Ɩ�������Ă��܂��B

����ɑ΂��Alambda�����g���āAa,d�������Ƃ��Ď󂯎�肻�̘a��Ԃ������֐����L�q����ƁE�E�E

	lambda a,b : a+b

�ƂȂ�܂��B

�ŏ��́ulambda�v�͗\���Łu���ꂩ��lambda���Ŗ����֐����`����v�Ƃ�������\���Ă��܂��B
def�Ɏ��Ă��܂����Adef�����O�t���̊֐����`����̂ɑ΂��Alambda�͖����̊֐����`���܂��B

lambda�ׂ̗ɂ��� a,b �͈�����\���A`def func(a,b):`�̃J�b�R�̒��Ɠ����Ӗ��������Ă��܂��B  
���Ȃ݂ɁA�����̓J���}�ŋ�؂�Ε����g���܂����A�����������Ă��\���܂���B

�R����������ŉE���� a+b ���Ԃ�l��\���A`return a+b`�Ɠ����Ӗ��ł��B  
�߂�l�͕K�������Ȃ��Ă͂����܂���B


### lambda���g�������b�g

lambda���g�������b�g�́A�R�[�h���Ȍ��ɏ����邱�Ƃ��������܂��B

��Ƃ��ėl�X�ȏ��i�̉��i�𔲂��o�������X�g������A���̃��X�g���炠����z�ȏ�̂��̂𔲂��o���A
���i�̈������ɕ��ׂ������擾����v���O��������������Ƃ��܂��B

lambda����p���Ȃ��ꍇ�̎������@�̗�

	prices = [3000,2500,10500,4300]
	paymentList = []
	for price in prices:
	    if price > 3500:
	        paymentList.append(price)
	
	paymentList.sort()
	
	print(paymentList)
 
���s����

	[4300, 10500]

�����lambda����p���ď����ƈȉ��̂悤�ɂȂ�܂��B

	prices = [3000,2500,10500,4300]
	priceList = list(filter(lambda price:price > 3500, prices))
	priceList.sort()
	
	print(priceList)
 
���s����

	[4300, 10500]

��L�T���v���ɂ�lambda���ƍ��킹��list�֐���filter�֐����g�p���܂����B
list�֐��͈����̒l��list�^�֕ϊ����A���̌�Asort()�֐��ɂĕ��ёւ����s�����߂Ɏg�p���Ă��܂��B
�����āAfilter�֐��͑������Ɏw�肳�ꂽ�z��̊e�v�f�ɑ΂��āA�������̊֐����������{���A
True�ƂȂ���̂����𒊏o���鏈�����s���Ă��܂��B

