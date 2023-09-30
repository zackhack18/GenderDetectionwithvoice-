# GenderDetectionwithvoice-
#Created by Zackhack18

import os

import pickle

Import warnings

import numpy as np

from FeaturesExtractor import FeaturesExtractor


warnings.filterwarnings("ignore")

class Gender Identifier:

def __init__(self, females_files_path, males_files_path, females_model_path, males_model_path):

self.females_training_path = Females_files_path

self.males training path = males_files_path

self.error

self.total sample

self.features extractor

FeaturesExtractor()

load models

self.females_gmm = pickle.load(open(females_model_path, 'rb')) self.males gmm = pickle.load(open(males_model_path, 'rb'))

def

process(self):

files self.get_file_pathsf self.females training path, self.males_training_path

)

read the tear directory and get the list of test and by Teles

for file in files:

self.total sample += 1

print("105 85 15" ("--> TESTING", ":", os.path.basename(fite)))

vector = self.features extractor.extract features(file) winner self. Identify gender(vector)

expected gender file.split("/")[1][-]

print("%10s 65 %1" % (+ EXPECTATION", ":", expected_gender))

print("%10s 3s 1s (+ IDENTIFICATION"

winner )

if winner != expected gender: self.error == 10 print("

accuracy accuracy_msg = **** Accuracy = " + str(round(accuracy, 3)) + "*****

(float(self.total sample self.error) / float(selt.total sample)) + 100

print(accuracy_msg
