// Toggle Journal and Planner modes
document.getElementById('journalbtn').addEventListener('click', () => {
  document.getElementById('journalSection').classList.remove('hidden');
  document.getElementById('plannerSection').classList.add('hidden');
});

document.getElementById('plannerbtn').addEventListener('click', () => {
  document.getElementById('plannerSection').classList.remove('hidden');
  document.getElementById('journalSection').classList.add('hidden');
});

// Mood/theme switching
document.querySelectorAll('.mood-btn').forEach(btn => {
  btn.addEventListener('click', () => {
    const theme = btn.getAttribute('data-theme');
    document.body.className = theme;
  });
});
window.addEventListener('DOMContentLoaded', () => {
  const dateTimeSpan = document.getElementById('currentDateTime');
  function updateDateTime() {
    const now = new Date();
    const options = { year: 'numeric', month: 'long', day: 'numeric' };
    const dateStr = now.toLocaleDateString(undefined, options);
    const timeStr = now.toLocaleTimeString();
    dateTimeSpan.innerHTML= `${dateStr}<br>${timeStr}`;
  }
  updateDateTime();
  setInterval(updateDateTime, 1000);
});

// Add task functionality (optional)
document.getElementById('addTaskBtn').addEventListener('click', () => {
  const input = document.getElementById('taskInput');
  const textarea = document.getElementById('task-list');
  const taskText = input.value.trim();
  if (taskText !== '') {
    textarea.value +=( textarea.value ? '\n' : '') + taskText;
    input.value = '';
  }
});