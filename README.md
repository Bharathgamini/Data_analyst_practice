# The analysis

## Here is th readme for the top demandskill for data analyst

view my book here: [skills_count.ipynb](Job_Project/skills_count.ipynb)

visualize data:
'''python
fig, ax = plt.subplots(len(job_titles), 1)
sns.set_theme(style ='ticks')

for i, jobtitle in enumerate(job_titles):
    df_plot = df_skills_percent[df_skills_percent['job_title_short']==jobtitle].head()
    sns.barplot(data= df_plot, y='job_skills', x='skill_percent',ax = ax[i],  hue='skill_count', palette = 'dark:b_r')
    ax[i].set_title(jobtitle)
    ax[i].set_ylabel('')
    ax[i].set_xlabel('')
    ax[i].get_legend().remove()
    ax[i].set_xlim(0,78)
    ax[i].legend().set_visible(False)
    for n,v in enumerate(df_plot['skill_percent']):
        ax[i].text(v +1,n,f'{v:.0f}%', va='center')
    if i!=len(job_titles)-1:
        ax[i].set_xticks([])
fig.suptitle('count of jobs per job title')
plt.tight_layout()

plt.show()

'''

### Reults
![text](Job_Project/skills_count_images/output.png)


### insights
python is a versatile skill and highly demanded for allthe roles that we did analysis
