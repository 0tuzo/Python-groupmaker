
def propose(student, groups):
    """
    Assign a student to their preferred group if there's capacity.
    If the preferred group is full, try the next priority group.
    """
    for choice in student['priority']:
        if len(groups[choice]['students']) < groups[choice]['capacity']:
            groups[choice]['students'].append(student)
            return

def assign_groups(students, groups):
    for student in students:
        propose(student, groups)


groups = {
    'Basketball': {'capacity': 10, 'students': []},
    'Unihockey': {'capacity': 10, 'students': []},
    'Fussball amb': {'capacity': 10, 'students': []},
    'Fussball nicht amb': {'capacity': 10, 'students': []},
    'Ultimate': {'capacity': 10, 'students': []}
}


students = [
     {'name': 'Yannis', 'gender': 'male', 'priority': ['Basketball', 'Unihockey', 'Fussball amb']},
    {'name': 'Mirko', 'gender': 'male', 'priority': ['Unihockey', 'Fussball amb', 'Ultimate']},
    {'name': 'Gaji', 'gender': 'male', 'priority': ['Fussball amb', 'Fussball nicht amb', 'Ultimate']},
    {'name': 'Shahin', 'gender': 'male', 'priority': ['Basketball', 'Fussball amb', 'Ultimate']},
    {'name': 'Sabri', 'gender': 'male', 'priority': ['Unihockey', 'Fussball nicht amb', 'Ultimate']},
    {'name': 'Luciano', 'gender': 'male', 'priority': ['Basketball', 'Unihockey', 'Fussball nicht amb']},
    {'name': 'Tarun', 'gender': 'male', 'priority': ['Basketball', 'Fussball nicht amb', 'Ultimate']},
    {'name': 'Michael', 'gender': 'male', 'priority': ['Unihockey', 'Fussball amb', 'Fussball nicht amb']},
    {'name': 'Simon', 'gender': 'male', 'priority': ['Basketball', 'Unihockey', 'Ultimate']},
    {'name': 'Lendrit', 'gender': 'male', 'priority': ['Fussball amb', 'Fussball nicht amb', 'Ultimate']},
    {'name': 'Shirin', 'gender': 'female', 'priority': ['Basketball', 'Fussball amb', 'Fussball nicht amb']},
    {'name': 'Alina', 'gender': 'female', 'priority': ['Unihockey', 'Fussball amb', 'Fussball nicht amb']},
    {'name': 'Nithusha', 'gender': 'female', 'priority': ['Basketball', 'Unihockey', 'Fussball amb']},
    {'name': 'Diana', 'gender': 'female', 'priority': ['Fussball nicht amb', 'Ultimate', 'Basketball']},
    {'name': 'Alegria', 'gender': 'female', 'priority': ['Unihockey', 'Fussball nicht amb', 'Fussball amb']},
    {'name': 'Nhaslit', 'gender': 'female', 'priority': ['Basketball', 'Fussball amb', 'Fussball nicht amb']},
    {'name': 'Sara', 'gender': 'female', 'priority': ['Unihockey', 'Ultimate', 'Fussball amb']},
    {'name': 'Lynn', 'gender': 'female', 'priority': ['Basketball', 'Fussball nicht amb', 'Fussball amb']},

    {'name': 'Riana', 'gender': 'female', 'priority': ['Unihockey', 'Fussball amb', 'Fussball nicht amb']},
    {'name': 'Melisa', 'gender': 'female', 'priority': ['Basketball', 'Ultimate', 'Fussball amb']},
    {'name': 'Ylenia', 'gender': 'female', 'priority': ['Fussball nicht amb', 'Ultimate', 'Unihockey']},
    {'name': 'Lara', 'gender': 'female', 'priority': ['Basketball', 'Fussball amb', 'Fussball nicht amb']},
    {'name': 'Amina', 'gender': 'female', 'priority': ['Unihockey', 'Fussball nicht amb', 'Ultimate']},
    {'name': 'Erijona', 'gender': 'female', 'priority': ['Basketball', 'Fussball amb', 'Ultimate']},
    {'name': 'Elmerida', 'gender': 'female', 'priority': ['Fussball nicht amb', 'Ultimate', 'Basketball']},
    {'name': 'Lina', 'gender': 'female', 'priority': ['Unihockey', 'Fussball amb', 'Fussball nicht amb']},
    {'name': 'Alken', 'gender': 'male', 'priority': ['Basketball', 'Unihockey', 'Fussball nicht amb']},
    {'name': 'Valan', 'gender': 'male', 'priority': ['Fussball amb', 'Fussball nicht amb', 'Ultimate']},
    {'name': 'Rohan', 'gender': 'male', 'priority': ['Basketball', 'Fussball nicht amb', 'Ultimate']},
    {'name': 'Simran', 'gender': 'male', 'priority': ['Unihockey', 'Fussball amb', 'Ultimate']},
    {'name': 'Arijon', 'gender': 'male', 'priority': ['Basketball', 'Ultimate', 'Fussball nicht amb']},
    {'name': 'Wiliam', 'gender': 'male', 'priority': ['Fussball amb', 'Ultimate', 'Unihockey']},
    {'name': 'Berat', 'gender': 'male', 'priority': ['Basketball', 'Fussball amb', 'Fussball nicht amb']},
 
   {'name': 'Beatriz', 'gender': 'female', 'priority': ['Unihockey', 'Fussball nicht amb', 'Fussball amb']},
   {'name': 'Noémi', 'gender': 'female', 'priority': ['Basketball', 'Unihockey', 'Ultimate']},
   {'name': 'Loreana', 'gender': 'female', 'priority': ['Fussball nicht amb', 'Ultimate', 'Fussball amb']},
   {'name': 'Ana', 'gender': 'female', 'priority': ['Unihockey', 'Fussball amb', 'Fussball nicht amb']},
   {'name': 'Alica', 'gender': 'female', 'priority': ['Basketball', 'Fussball nicht amb', 'Fussball amb']},
   {'name': 'Tenzin', 'gender': 'female', 'priority': ['Unihockey', 'Fussball nicht amb', 'Ultimate']},
   {'name': 'Ronja', 'gender': 'female', 'priority': ['Basketball', 'Fussball amb', 'Ultimate']},
   {'name': 'Jannis', 'gender': 'male', 'priority': ['Fussball nicht amb', 'Ultimate', 'Basketball']},
   {'name': 'James', 'gender': 'male', 'priority': ['Unihockey', 'Fussball amb', 'Fussball nicht amb']},
   {'name': 'Hugo', 'gender': 'male', 'priority': ['Basketball', 'Unihockey', 'Fussball nicht amb']},
   {'name': 'Nicola', 'gender': 'male', 'priority': ['Fussball amb', 'Fussball nicht amb', 'Ultimate']},
   {'name': 'Gevin', 'gender': 'male', 'priority': ['Basketball', 'Fussball nicht amb', 'Ultimate']},
   {'name': 'Belal', 'gender': 'male', 'priority': ['Fussball amb', 'Fussball nicht amb', 'Ultimate']},
   {'name': 'Bleron', 'gender': 'male', 'priority': ['Unihockey', 'Fussball amb', 'Ultimate']},
   {'name': 'Jan', 'gender': 'male', 'priority': ['Basketball', 'Ultimate', 'Fussball nicht amb']},
   {'name': 'Andrin', 'gender': 'male', 'priority': ['Fussball amb', 'Ultimate', 'Unihockey']},
]


assign_groups(students, groups)


def split_students_within_group(group_name, group_students, subgroup_size):
    num_subgroups = len(group_students) // subgroup_size
    subgroups = [group_students[i:i + subgroup_size] for i in range(0, len(group_students), subgroup_size)]

    # If the last subgroup has only one student, merge it with the previous subgroup
    if len(subgroups[-1]) == 1:
        subgroups[-2].append(subgroups[-1][0])
        subgroups.pop()

    return [(f"{group_name} Subgroup {i + 1}", subgroup) for i, subgroup in enumerate(subgroups)]

# Split students within each group into subgroups of size 3 (adjust as needed)
subgroup_size = 3
for group_name, group_data in groups.items():
    group_students = group_data['students']
    subgroups = split_students_within_group(group_name, group_students, subgroup_size)
    group_data['students'] = subgroups

# Display the updated group assignments
for group_name, group_data in groups.items():
    print(f"{group_name}:")
    for subgroup_name, subgroup_students in group_data['students']:
        print(f"  {subgroup_name}: {', '.join(student['name'] for student in subgroup_students)}")
