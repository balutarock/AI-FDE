
## level 1

#### Questions: 
1. Introduction
2.  Difference between UseState and UseEffect

### Coding Questions
1. Reverse string
2. Frequency of characters
3. Remove Adjecent Characters after add score.
```
// const s = "balu";
// const lengthOfS= s.length

// let revString=""
// for(i=0; i< lengthOfS; i++){
//     revString+= s[(lengthOfS-1)-i]
// }

// console.log("revString >> ", revString)

// Given a string, return an object containing the count of each character. 
// Input: "aabbc"
// Output: { a: 2, b: 2, c: 1 }

// const str='aabbc';
// const lengthOfS= str.length
// let result={}

// for(i=0; i< lengthOfS; i++){
//     if(result[str[i]]===undefined){
//         result[str[i]] = 1
//     }else{
//         result[str[i]] = result[str[i]] +1
//     }
// }

// console.log("result >> ", result)


// Given a string of lowercase letters, if two adjacent characters are the same, you can remove them and score 1 point.
// After removing a pair, the remaining characters join together and may form new adjacent matching pairs.
// What is the maximum score you can achieve by repeatedly removing adjacent matching character pairs?

// Example

// Input: abccbda
// Output:2

// Explanation:
// Remove "cc" → "abbda" (score = 1)
// Remove "bb" → "ada" (score = 2)
// No more pairs → total = 2

// #	Input	Expected Output
// 1	aa	          1
// 2	aaaa	    

      2
// 3	abcde	          0
// 4	abccbda	          2
// 5	aabbaa	          3

// const str= "aaaa";
// let lengthOfS= str.length
// let score = 0
// let newStr=""

// function adjecentChar(s){
//     for(i=0; i< lengthOfS-1; i++){
//         // check two adjecent string
//         if(s[i]===s[i+1]){
//             score+=1
//             // console.log("adjecent >> ", s[i]===s[i+1], s[i],s[i+1])
//             // remove the ajecent
//             newStr=str.slice(0,i) + str.slice(i+2,lengthOfS)
//             // console.log(str.slice(i+2,lengthOfS))
//             lengthOfS=newStr.length
//             adjecentChar(newStr)
//             // console.log("new String >> ", newStr)
//         }
//     }
// }

// adjecentChar(str)
// console.log(score)
```

## Level 2

### Assignment: Job portal page: 
The page should take the personal info and profissinal info
#### personal info: 
1. fullname
2. email

#### Profissional info
1. associated skills with relevant experince

#### Code 
```
import "./styles.css";

import { useState } from "react";

import SkillsList from "./skills-list";

  

const profileInfo = {

fullName: "",

email: "",

skills: [],

};

  

export default function App() {

const [profile, setProfile] = useState(profileInfo);

const [skill, setSkill] = useState("");

const [exp, setExp] = useState("");

  

const onChangeFullName = (e) => {

const value = e.target.value;

const updatedData = { ...profile };

updatedData["fullName"] = value;

setProfile(updatedData);

};

  

const onChangeEmail = (e) => {

const value = e.target.value;

const updatedData = { ...profile };

updatedData["email"] = value;

setProfile(updatedData);

};

  

const onChangeSkill = (e) => {

const value = e.target.value;

setSkill(value);

};

  

const onChangeExp = (e) => {

const value = e.target.value;

setExp(value);

};

  

const onClickAddSkill = () => {

const Updatedskills = {

id: profile.skills.length + 1,

skill: skill,

experience: exp,

};

const updatedData = { ...profile };

updatedData["skills"] = [...profile.skills, Updatedskills];

setProfile(updatedData);

setSkill("");

setExp("");

};

  

const onEditSkill = (id) => {

console.log("id >> ", id);

console.log("profile.skills >> ", profile.skills);

  

const filterdata = profile.skills.filter((each) => each.id === id);

setSkill(filterdata[0].skill);

setSkill(filterdata[0].experience);

};

  

// const updatedSkills = profile.skills.map((each) =>

// each.id === id ? { skill: skill, experience: exp, ...each } : each

// );

// const updatedData = { ...profile };

// updatedData["skills"] = updatedSkills;

// setProfile(updatedData);

  

return (

<div className="App">

{/* Person Info */}

<div>

<label>Enter Full Name</label>

<input

type="text"

value={profile.fullName}

onChange={(e) => onChangeFullName(e)}

/>

</div>

<div>

<label>Enter Email</label>

<input

type="text"

value={profile.email}

onChange={(e) => onChangeEmail(e)}

/>

</div>

{/* Skills */}

<div>

<label>Enter Skill</label>

<input type="text" value={skill} onChange={(e) => onChangeSkill(e)} />

</div>

<div>

<label>Years of Expericne in the skill</label>

<input type="text" value={exp} onChange={(e) => onChangeExp(e)} />

</div>

<div>

<button onClick={onClickAddSkill}>Add Skills</button>

</div>

{/* List of Skills */}

<div>

{profile.skills.map((each) => (

<SkillsList skill={each} onEditSkill={onEditSkill} />

))}

</div>

</div>

);

}
```