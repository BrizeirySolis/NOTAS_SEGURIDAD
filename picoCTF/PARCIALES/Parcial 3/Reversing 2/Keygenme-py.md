## Introducción
[keygenme-trial.py](https://mercury.picoctf.net/static/fb75b48f9214cf992a2199b5785564e7/keygenme-trial.py)
## Descripción
import hashlib

key_part_static1_trial = "picoCTF{1n_7h3_|<3y_of_"
#key_part_dynamic1_trial = "xxxxxxxx"
key_part_static2_trial = "}"

temp = hashlib.sha256(b"FREEMAN").hexdigest()
key_part_dynamic1_trial = temp[4]+temp[5]+temp[3]+temp[6]+temp[2]+temp[7]+temp>
key_full_template_trial = key_part_static1_trial+key_part_dynamic1_trial+key_p>

print(key_full_template_trial)


nano solver.py : codigo de arriba
python3 solver.py 

## Solución 
picoCTF{1n_7h3_|<3y_of_0d208392}
