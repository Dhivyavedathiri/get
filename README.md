Your Answer

import axios from 'axios';



const getUserDetails = async () => {

 try {

  const response = await axios.get('https://crudcrud.com/api/7c3a20c5eadb480599a0d133a7b52731/appointments');

   

  if (response.status === 200) {

   const userAppointments = response.data;

   updateUI(userAppointments);

  } else {

   console.error('Failed to retrieve user details from the cloud.');

  }

 } catch (error) {

  console.error('Error making the GET request:', error);

 }

};



const updateUI = (userAppointments) => {

};



document.addEventListener('DOMContentLoaded', () => {

 getUserDetails();

});
