# for linux ig
import sys
from PySide6 import QtCore as qtc
from PySide6 import QtWidgets as qtw
from PySide6 import QtGui as qtg
# from PySide6 import *
# import subprocess as sp
import os

class Main(qtw.QWidget):
	
	def __init__(self):
		super().__init__()
		self.setWindowTitle("choose ur file(s) to convert")
		self.setStyleSheet("background-color:#232020;")
		self.dsgmain()
		self.show()
	def dsgmain(self):
		self.f = ''
		self.TTL = qtw.QLabel(self)
		self.TTL.move(20,10)
		self.TTL.resize(1400,20)
		self.TTL.setText("__Stupid Media Format Converter ver b0.0.1 ______________________________________________________________")
		self.OpListffmpeg = [
		".mp4",".mp3",".wav",
		".flac",".ogg",".oga",
		".wma",".avi",".mov",
		".dts",".avchd",".lpcm",
		".dsd",".aiff",".asf",".wmv"
		]
		# self.mainfr = qtw.QFrame(self)
		# self.mainfr.setFrameShape(qtw.QFrame.Box)
		# self.mainfr.setLineWidth(2)
		# self.mainfr.move(5,15)
		# self.mainfr.resize(630,420)
		# self.mainfr.setStyleSheet("""
		# 	QFrame {
		#  		color: #FFc3aB;
		#     	background: transparent;
		# 		}
		# 	""")
		self.cc = qtw.QComboBox(self)
		self.cc.addItem("Choose your format")
		self.cc.move(400,100)
		self.cc.addItems(self.OpListffmpeg)
		self.getcc = ""
		#self.debug = qtw.QPushButton(self)
		#self.debug.setText("sfsd")
		#self.debug.clicked.connect(self.de)
		self.Browsebut = qtw.QPushButton(self)
		self.Browsebut.setText("Browse")
		self.Browsebut.move(50,100)
		self.Browsebut.clicked.connect(self.browse)
		self.process = qtw.QPushButton(self)
		self.process.setText("⟶")
		self.process.move(400,200)
		self.process.clicked.connect(self.RES)
		self.dirl = qtw.QLabel(self)
		self.dirl.setText("in-dir-> ")
		self.dirl.move(50,300)
		self.dirl.resize(1,31)
		self.dirlo = qtw.QLabel(self)
		self.dirlo.setText("out-dir-> ")
		self.dirlo.move(50,350)
		self.dirlo.resize(1,31)
		self.out = qtw.QPushButton(self)
		self.out.setText("Save As")
		self.out.move(50,150)
		self.chk = 0
		self.out.clicked.connect(self.outloc)
		self.ffmpeg_i = qtw.QPushButton(self)
		self.ffmpeg_i.setText("Insall ffmpeg")
		self.ffmpeg_i.move(50, 650)
		self.ffmpeg_i.resize(130,35)
		self.ffmpeg_i.clicked.connect(self.ffmpeg_installbutt)
		self.fr =qtw.QFrame(self)
		self.fr.setFrameShape(qtw.QFrame.Box )
		#self.fr.setFrameStyle(qtw.QFrame.StyledPanel)
		self.fr.setLineWidth(1.5)
		self.fr.move(30,270)
		self.fr.resize(5,0)
		self.fr.setStyleSheet("""
			QFrame {
		 		color: #FFc3aB;
		    	background: transparent;
				}
			""")
		#self.fr.addWidget(self.dirl | self.dirlo)
		self.apl = qtw.QPushButton(self)
		self.apl.setText("Apply")
		self.apl.move(400,150)
		self.apl.clicked.connect(self.apply)
		#### anim stuff
		#anim dirlo/dirl
		self.anim13dirs = qtc.QPropertyAnimation(self.dirl, b"pos")
		self.anim14dirs = qtc.QPropertyAnimation(self.dirl, b"size")
		self.anim13dirs.setEndValue(qtc.QPoint(50,300))
		self.anim14dirs.setEndValue(qtc.QSize(182,31))
		self.animg2dirs = qtc.QSequentialAnimationGroup()
		self.animg2dirs.addAnimation(self.anim13dirs)
		self.animg2dirs.addAnimation(self.anim14dirs)
		self.anim13dirlos = qtc.QPropertyAnimation(self.dirlo, b"pos")
		self.anim14dirlos = qtc.QPropertyAnimation(self.dirlo, b"size")
		self.anim13dirlos.setEndValue(qtc.QPoint(50,350))
		self.anim14dirlos.setEndValue(qtc.QSize(182,31))
		self.animg2dirs.addAnimation(self.anim13dirlos)
		self.animg2dirs.addAnimation(self.anim14dirlos)
		self.anim13dirs.setDuration(900)
		self.anim13dirlos.setDuration(100)
		self.anim14dirs.setDuration(1000)
		self.anim14dirlos.setDuration(1100)
		self.animg2dirs.start()
		#anim box
		self.anim133s = qtc.QPropertyAnimation(self.fr, b"size")
		self.anim143s = qtc.QPropertyAnimation(self.fr, b"size")
		self.anim133s.setEndValue(qtc.QSize(5,130))
		self.anim143s.setEndValue(qtc.QSize(750,130))
		self.animg23s = qtc.QSequentialAnimationGroup()
		self.animg23s.addAnimation(self.anim133s)
		self.animg23s.addAnimation(self.anim143s)
		self.anim133s.setDuration(800)
		self.anim143s.setDuration(1300)
		self.animg23s.start()
	def apply(self):
		self.anim13s = qtc.QPropertyAnimation(self.apl, b"pos")
		self.anim14s = qtc.QPropertyAnimation(self.apl, b"pos")
		self.anim13s.setEndValue(qtc.QPoint(400,153))
		self.anim14s.setEndValue(qtc.QPoint(400,150))
		self.animg2s = qtc.QSequentialAnimationGroup()
		self.animg2s.addAnimation(self.anim13s)
		self.animg2s.addAnimation(self.anim14s)
		self.anim13s.setDuration(100)
		self.anim14s.setDuration(100)
		self.animg2s.start()
		# self.ff1 = str(self.f[0])
		self.getcc = str(self.cc.currentText())
		# self.rmovslash1 = self.ff1.replace('/',' ')
		# self.rmovdot1 = self.rmovslash1.replace('.',' ')
		# self.li1 = list(self.rmovdot1.split(" "))
		# self.slic1 = self.li1[:-1]
		# print(self.li1)
		# self.addsls = str(' '.join(self.slic1)).replace(' ','/') 
		# self.final1 = self.addsls
		if self.chk == 1:
			self.dirlo.setText(f"out-dir->{self.af}"+f"{self.getcc}")
		else:
			try:
				self.dirlo.setText(f"out-dir->{self.final}"+f"{self.getcc}")
				self.dirlo.adjustSize()
			except:pass
	def RES(self):
		self.anim13 = qtc.QPropertyAnimation(self.process, b"pos")
		self.anim14 = qtc.QPropertyAnimation(self.process, b"pos")
		# self.anim.setEndValue(qtc.QSize(82, 31))
		# self.anim2.setEndValue(qtc.QSize(82,31))
		self.anim13.setEndValue(qtc.QPoint(400, 203))
		self.anim14.setEndValue(qtc.QPoint(400,200))
		self.animg2 = qtc.QSequentialAnimationGroup()
		
		self.animg2.addAnimation(self.anim13)
		self.animg2.addAnimation(self.anim14)
		#self.anim.setEasingCurve(qtc.QEasingCurve.OutBounce)
		self.anim13.setDuration(100)
		self.anim14.setDuration(100)
		self.animg2.start()

		if self.chk == 1:
			self.getcc = str(self.cc.currentText())
			print(f"ffmpeg -i {self.ff} " + f"{self.af}"+ f"{self.getcc}")
			os.system(f"ffmpeg -i {self.ff} " + f"{self.af}"+f"{self.getcc}")
			
		else:
			#print(f"ffmpeg -i {self.ff} {self.final}"+"(x)"+ f"{self.getcc}") 
			os.system(f"ffmpeg -i {self.ff} {self.final}"+"x"+ f"{self.getcc}")
	def ffmpeg_installbutt(self):
		passw = ""
		with open("sudopass.txt","r") as p:
			for cv in p: passw += p
		os.system('echo %s|sudo -S %s' % (passw, 'apt install ffmpeg'))
	def browse(self):
		self.anim11 = qtc.QPropertyAnimation(self.Browsebut, b"pos")
		self.anim12 = qtc.QPropertyAnimation(self.Browsebut, b"pos")
		# self.anim.setEndValue(qtc.QSize(82, 31))
		# self.anim2.setEndValue(qtc.QSize(82,31))
		self.anim11.setEndValue(qtc.QPoint(50, 103))
		self.anim12.setEndValue(qtc.QPoint(50,100))
		self.animg1 = qtc.QSequentialAnimationGroup()
		
		self.animg1.addAnimation(self.anim11)
		self.animg1.addAnimation(self.anim12)
		#self.anim.setEasingCurve(qtc.QEasingCurve.OutBounce)
		self.anim11.setDuration(100)
		self.anim12.setDuration(100)
		self.animg1.start()
		#self.out.resize(80,25)
		self.getcc = str(self.cc.currentText())
		self.f = qtw.QFileDialog.getOpenFileName(self)
		self.ff = str(self.f[0])
		print(self.f)
		print(self.ff)
		self.rmovslash = self.ff.replace('/',' ')
		self.rmovdot = self.rmovslash.replace('.',' ')
		self.li = list(self.rmovdot.split(" "))
		self.slic = self.li[:-1]
		print(self.li)
		self.addslashagainsussybaka = str(' '.join(self.slic)).replace(' ','/') 
		self.final = self.addslashagainsussybaka
		print(self.addslashagainsussybaka, self.final)
		self.dirl.setText(f"in-dir->{self.ff}")
		if self.getcc == "Choose your format":
			self.getcc = ".mp3"
		self.asd = "\n"
		self.dirlo.setText(f"out-dir->{self.final}""x"+f"{self.getcc}")
		self.dirl.adjustSize()
		self.dirlo.adjustSize()
		print(len(f"in-dir->{self.final}"))
		if len(f"in-dir->{self.final}") >= 80:
				print(self.final[:-int(len(self.final)-590/10)])
				self.dirlo.setText(f"out-dir->{self.final[:-int(len(self.final)-590/10)]+'...'}""x"+f"{self.getcc}")
				self.dirl.setText(f"in-dir->{self.final[:-int(len(self.final)-590/10)]+'...'}""x"+f"{self.getcc}")
				# self.anim143s.setEndValue(qtc.QSize(0,500))
				# self.animg23s.addAnimation(self.anim143s)
				# self.anim143s.setDuration(1300)

				# self.animg23s.start()

	def outloc(self):
		self.anim = qtc.QPropertyAnimation(self.out, b"pos")
		self.anim2 = qtc.QPropertyAnimation(self.out, b"pos")
		# self.anim.setEndValue(qtc.QSize(82, 31))
		# self.anim2.setEndValue(qtc.QSize(82,31))
		self.anim.setEndValue(qtc.QPoint(50, 153))
		self.anim2.setEndValue(qtc.QPoint(50,150))
		self.animg = qtc.QSequentialAnimationGroup()
		self.animg.addAnimation(self.anim)
		self.animg.addAnimation(self.anim2)
		#self.anim.setEasingCurve(qtc.QEasingCurve.OutBounce)
		self.anim.setDuration(100)
		self.anim2.setDuration(100)
		self.animg.start()
		#self.out.resize(80,25)
		self.chk = 1
		self.getcc = str(self.cc.currentText())
		print(self.getcc)
		if self.getcc not in self.OpListffmpeg:
			self.forgorform=qtw.QErrorMessage()
			self.forgorform.showMessage("Choose your format first")
		elif self.getcc in self.OpListffmpeg:
			self.dirn = qtw.QFileDialog.getSaveFileName(self, 'Save As')
			self.af = str(self.dirn[0])
			self.dirlo.setText(f"out-dir->{self.af}"+f"{self.getcc}")
			# if len(self.af) > 100:
			# 	self.anim143s.setEndValue(qtc.QSize(590,300))
			# 	self.animg23s.addAnimation(self.anim133s)
			# 	self.anim143s.setDuration(1300)
			# 	self.animg23s.start()

			self.dirlo.adjustSize()
			# self.fl = open(self.dirn,'open')
			# self.t = self.textEdit.toPlainText()
			# self.fl.write(self.t)
			# self.fl.close	

if __name__ == "__main__":
	a = qtw.QApplication([])
	a.setStyleSheet(
		""" 
		QPushButton {
		  border-radius:1px;
		  border: 1px solid #6f5f5f;
		  background: #ffffff;
		  color:#FFc3aB;
		  width:80px;
		  height:30px;
		  font-size:15px;
		 
		}
		QPushButton:hover {
		  border: 1px solid #FFc3aB;
		  background: transparent;
		  color:#FFc3aB;
		  font-size:15px;
		 
		}
	

		QLabel { 
		   	color:#FFc3aB; 
		   	font-size: 15px;
		   	background:#1d1d1d;

		   }
		 QComboBox {

		    color:#FFc3aB;
		    background:transparent;
		 }
		""")
	wg  = Main()
	wg.setFixedSize(850, 750)
	wg.show()
	sys.exit(a.exec()) 


