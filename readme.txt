### Dummy DataTable Begin

    <v-data-table
        :headers="[
          { text: 'FirstName', value: 'firstname' },
          { text: 'LastName', value: 'lastname' }
        ]"
        :items="[
          { firstname: 'lek', lastname: '123' },
          { firstname: 'kan', lastname: '555' }
        ]"
      >
      </v-data-table>
### Dummy DataTable End


#no sub-folder        
      location / {
          try_files $uri $uri/ /index.html;
      }   
        
# have sub-folder named "/"        
location / {
  try_files $uri $uri/ /index.html; 
}  