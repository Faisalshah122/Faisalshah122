
class Aneurysm:
    def __init__(self, aneurysm_type, location, size):
        self.aneurysm_type = aneurysm_type
        self.location = location
        self.size = size
        self.complications = []
        self.management_plan = []
        self.treatment_options = []
        self.prognosis = ""

    def define_types(self):
        """
        Defines types of aneurysms based on location and morphology.
        """
        types = {
            "Cerebral": "Aneurysms occurring in the brain, such as saccular (berry), fusiform, and dissecting aneurysms.",
            "Aortic": "Aneurysms in the aorta, including thoracic, abdominal, and thoracoabdominal.",
            "Peripheral": "Aneurysms in other arteries, e.g., popliteal, femoral.",
        }
        return types

    def identify_complications(self):
        """
        Lists possible complications of aneurysms.
        """
        self.complications = [
            "Rupture leading to hemorrhage",
            "Compression of adjacent structures",
            "Thrombosis formation",
            "Embolization causing ischemia in downstream vessels",
        ]
        return self.complications

    def management_plan_outline(self):
        """
        Outlines management plan based on aneurysm type and characteristics.
        """
        self.management_plan = [
            "Regular monitoring with imaging for small, asymptomatic aneurysms",
            "Risk factor modification, e.g., control of hypertension, smoking cessation",
            "Surgical or endovascular intervention for symptomatic or large aneurysms",
        ]
        return self.management_plan

    def treatment_options(self):
        """
        Outlines treatment options for aneurysms.
        """
        self.treatment_options = [
            "Endovascular coiling or flow diversion (especially in cerebral aneurysms)",
            "Surgical clipping or open repair (often used in cerebral and large aortic aneurysms)",
            "Stent grafting for aortic aneurysms",
        ]
        return self.treatment_options

    def set_prognosis(self):
        """
        Sets prognosis based on type, location, and management outcome.
        """
        if self.aneurysm_type == "Cerebral" and self.size > 7:
            self.prognosis = "High risk of rupture; requires timely intervention for better outcome."
        elif self.aneurysm_type == "Aortic" and self.size > 5.5:
            self.prognosis = "Requires surgical management; good prognosis if treated before rupture."
        else:
            self.prognosis = "Generally good with monitoring and intervention as necessary."
        return self.prognosis

    def display_info(self):
        """
        Displays detailed information about the aneurysm.
        """
        return {
            "Type": self.aneurysm_type,
            "Location": self.location,
            "Size": f"{self.size} cm",
            "Complications": self.complications,
            "Management Plan": self.management_plan,
            "Treatment Options": self.treatment_options,
            "Prognosis": self.prognosis
        }

# Example usage:
aneurysm = Aneurysm("Cerebral", "Middle cerebral artery", 5)
aneurysm.define_types()
aneurysm.identify_complications()
aneurysm.management_plan_outline()
aneurysm.treatment_options()
aneurysm.set_prognosis()
info = aneurysm.display_info()

for key, value in info.items():
    print(f"{key}: {value}")
<!---
Faisalshah122/Faisalshah122 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
