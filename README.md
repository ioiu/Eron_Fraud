# Eron_Fraud
#!/usr/bin/python

import sys
import pickle
import pandas as pd
import numpy as np
sys.path.append("../tools/")

from feature_format import featureFormat, targetFeatureSplit
from tester import dump_classifier_and_data

# At first, I put all features except email_address into my features_list and I will extract them later.

features_list = ['poi','salary', 'bonus', 'deferral_payments', 'deferred_income', 'director_fees',
                 'exercised_stock_options', 'expenses', 'from_messages', 'from_poi_to_this_person',
                'from_this_person_to_poi', 'loan_advances', 'long_term_incentive', 'other',
                'restricted_stock', 'restricted_stock_deferred', 'shared_receipt_with_poi',
                'to_messages', 'total_payments', 'total_stock_value']
