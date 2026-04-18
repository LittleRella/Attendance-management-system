import React, { useState } from 'react';
import { 
  Activity, BarChart3, BookOpen, Users, Grid3X3, QrCode, 
  Download, Upload, ExternalLink, Edit3, Trash2, CheckCircle, 
  Smartphone, ShieldCheck, ChevronRight, X, Globe, UserCheck,
  Calendar, Clock, Filter, FileSpreadsheet
} from 'lucide-react';

const App = () => {
  // --- STATE ---
  const [activeView, setActiveView] = useState('overview');
  const [attendanceMode, setAttendanceMode] = useState('physical'); // 'physical' or 'virtual'
  const [toast, setToast] = useState({ visible: false, message: '' });
  
  // Temporal & Group Filters State
  const [filters, setFilters] = useState({
    semester: 'Semester 1',
    year: '2024',
    month: 'January',
    date: new Date().toISOString().split('T')[0],
    cohort: 'MMBA 10',
    course: 'BUS701'
  });

  const [students, setStudents] = useState([
    { id: 's1', matric: '24/MMBA/001', fname: 'Sarah', lname: 'Ade', email: 'sarah.ade@edu.ng', phone: '+234 802 345 6789', cohort: 'MMBA 10', yield: 88 },
    { id: 's2', matric: '24/EMBA/012', fname: 'John', lname: 'Doe', email: 'j.doe@corp.com', phone: '+234 810 123 4567', cohort: 'EMBA 31', yield: 72 },
    { id: 's3', matric: '24/MEM/045', fname: 'Grace', lname: 'Eze', email: 'grace@edu.ng', phone: '+234 703 987 6543', cohort: 'MEMBA 13', yield: 95 },
    { id: 's4', matric: '24/MMBA/002', fname: 'David', lname: 'Okon', email: 'david@gmail.com', phone: '+234 905 555 1234', cohort: 'MMBA 6', yield: 64 }
  ]);

  const [editingStudent, setEditingStudent] = useState(null);

  // --- CONFIGURATION DATA ---
  const generateRange = (prefix, start, end) => {
    const arr = [];
    for (let i = start; i <= end; i++) {
      arr.push(`${prefix} ${i}`);
    }
    return arr;
  };

  const ALL_COHORTS = [
    ...generateRange("MMBA", 6, 20),
    ...generateRange("MEMBA", 13, 20),
    ...generateRange("EMBA", 31, 40)
  ];

  const SEMESTERS = ["Semester 1", "Semester 2", "Summer"];
  const YEARS = ["2023", "2024", "2025"];
  const MONTHS = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
  
  const courses = [
    { id: 'c1', code: 'BUS701', name: 'Strategic Management' },
    { id: 'c2', code: 'FIN702', name: 'Corporate Finance' },
    { id: 'c3', code: 'MKT703', name: 'Digital Marketing' },
    { id: 'c4', code: 'OPS704', name: 'Operations Logic' }
  ];

  // --- ACTIONS ---
  const showToast = (msg) => {
    setToast({ visible: true, message: msg });
    setTimeout(() => setToast({ visible: false, message: '' }), 3000);
  };

  const handleFilterChange = (key, value) => {
    setFilters(prev => ({ ...prev, [key]: value }));
  };

  const downloadCSVTemplate = () => {
    const headers = "FirstName,LastName,MatricNo,Email,Phone,Cohort,CourseCode\n";
    const blob = new Blob([headers], { type: 'text/csv' });
    const url = window.URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.setAttribute('hidden', '');
    a.setAttribute('href', url);
    a.setAttribute('download', 'attendx_student_template.csv');
    document.body.appendChild(a);
    a.click();
    document.body.removeChild(a);
    showToast("Template downloaded successfully.");
  };

  const deleteStudent = (id) => {
    setStudents(students.filter(s => s.id !== id));
    showToast("Student record deleted successfully.");
  };

  return (
    <div className="flex min-h-screen bg-[#f1f5f9] text-slate-900 font-['Inter']">
      {/* Sidebar */}
      <aside className="w-[280px] bg-[#0b0f1a] text-white fixed h-full flex flex-col p-8 z-40">
        <div className="flex items-center gap-3 mb-12">
          <div className="bg-blue-600 p-2.5 rounded-xl shadow-lg shadow-blue-500/30">
            <Activity className="w-6 h-6" />
          </div>
          <h1 className="font-black text-2xl tracking-tighter uppercase">AttendX</h1>
        </div>
        
        <nav className="space-y-1.5 flex-1">
          {[
            { id: 'overview', icon: <BarChart3 className="w-5 h-5" />, label: 'Dashboard' },
            { id: 'courses', icon: <BookOpen className="w-5 h-5" />, label: 'Manage Courses' },
            { id: 'registry', icon: <Users className="w-5 h-5" />, label: 'Student Registry' },
            { id: 'matrix', icon: <Grid3X3 className="w-5 h-5" />, label: 'Session Matrix' },
          ].map(item => (
            <button 
              key={item.id}
              onClick={() => setActiveView(item.id)}
              className={`w-full flex items-center gap-4 px-5 py-4 rounded-2xl transition-all font-bold text-sm text-left ${activeView === item.id ? 'bg-blue-600 text-white shadow-xl shadow-blue-500/20' : 'text-slate-400 hover:bg-white/5'}`}
            >
              {item.icon} {item.label}
            </button>
          ))}
        </nav>

        <button 
          onClick={() => setActiveView('activate')}
          className={`w-full mt-auto py-5 rounded-2xl font-black text-sm tracking-wide flex items-center justify-center gap-3 transition-all ${activeView === 'activate' ? 'bg-blue-600 text-white shadow-xl shadow-blue-900/40' : 'bg-slate-800 text-slate-400'}`}
        >
          <QrCode className="w-5 h-5" /> GENERATE QR
        </button>
      </aside>

      {/* Main Content */}
      <main className="ml-[280px] flex-1 p-10">
        <header className="flex justify-between items-start mb-6">
          <div>
            <h2 className="text-4xl font-black tracking-tighter text-slate-900 capitalize">{activeView.replace('-', ' ')}</h2>
            <p className="text-slate-500 font-medium text-sm mt-1">Enterprise academic tracking & intelligence system.</p>
          </div>
        </header>

        {/* Global Filter Bar - Updated with Cohort/Course */}
        {(activeView === 'overview' || activeView === 'registry' || activeView === 'matrix') && (
          <div className="bg-white p-4 rounded-3xl shadow-sm border border-slate-100 flex flex-wrap gap-4 mb-10 items-center">
            <div className="flex items-center gap-2 px-4 border-r border-slate-100">
              <Filter className="w-4 h-4 text-slate-400" />
              <span className="text-[10px] font-black text-slate-400 uppercase">Filters</span>
            </div>
            
            <div className="flex flex-1 gap-4 overflow-x-auto pb-1 md:pb-0">
              <FilterSelect label="Cohort" value={filters.cohort} options={ALL_COHORTS} onChange={(v) => handleFilterChange('cohort', v)} />
              <FilterSelect label="Course" value={filters.course} options={courses.map(c => c.code)} onChange={(v) => handleFilterChange('course', v)} />
              <FilterSelect label="Semester" value={filters.semester} options={SEMESTERS} onChange={(v) => handleFilterChange('semester', v)} />
              <FilterSelect label="Year" value={filters.year} options={YEARS} onChange={(v) => handleFilterChange('year', v)} />
              <div className="flex flex-col">
                <span className="text-[9px] font-black text-slate-400 uppercase mb-1">Date</span>
                <input 
                  type="date" 
                  value={filters.date} 
                  onChange={(e) => handleFilterChange('date', e.target.value)}
                  className="bg-slate-50 border-none rounded-xl text-xs font-bold px-3 py-2 outline-none" 
                />
              </div>
            </div>
          </div>
        )}

        <div className="animate-in fade-in slide-in-from-bottom-4 duration-500">
          {activeView === 'overview' && <OverviewUI ALL_COHORTS={ALL_COHORTS} />}
          {activeView === 'courses' && <CourseUI courses={courses} />}
          {activeView === 'registry' && (
            <RegistryUI 
              students={students} 
              onDelete={deleteStudent} 
              onEdit={setEditingStudent}
              downloadCSVTemplate={downloadCSVTemplate}
            />
          )}
          {activeView === 'activate' && (
            <ActivateUI 
              ALL_COHORTS={ALL_COHORTS} 
              SEMESTERS={SEMESTERS}
              YEARS={YEARS}
              MONTHS={MONTHS}
              courses={courses} 
              showToast={showToast} 
              attendanceMode={attendanceMode}
              setAttendanceMode={setAttendanceMode}
              filters={filters}
              handleFilterChange={handleFilterChange}
            />
          )}
          {activeView === 'matrix' && <MatrixUI students={students} filters={filters} />}
        </div>
      </main>

      {/* Toast Notification */}
      {toast.visible && (
        <div className="fixed bottom-10 right-10 bg-slate-900 text-white px-8 py-5 rounded-2xl shadow-2xl flex items-center gap-4 z-[100] border border-white/10 animate-in fade-in slide-in-from-right-4">
          <CheckCircle className="w-5 h-5 text-blue-400" />
          <span className="text-sm font-bold">{toast.message}</span>
        </div>
      )}
    </div>
  );
};

// --- HELPER COMPONENTS ---

const FilterSelect = ({ label, value, options, onChange }) => (
  <div className="flex flex-col min-w-[120px]">
    <span className="text-[9px] font-black text-slate-400 uppercase mb-1">{label}</span>
    <select 
      value={value} 
      onChange={(e) => onChange(e.target.value)}
      className="bg-slate-50 border-none rounded-xl text-xs font-bold px-3 py-2 outline-none appearance-none cursor-pointer hover:bg-slate-100 transition-colors"
    >
      {options.map(opt => <option key={opt} value={opt}>{opt}</option>)}
    </select>
  </div>
);

const OverviewUI = ({ ALL_COHORTS }) => {
  const renderPie = (pct) => {
    const circumference = 2 * Math.PI * 18;
    const offset = circumference - (pct / 100) * circumference;
    return (
      <div className="relative w-20 h-20 flex items-center justify-center">
        <svg className="w-full h-full -rotate-90">
          <circle cx="50%" cy="50%" r="18" fill="transparent" stroke="#f1f5f9" strokeWidth="5" />
          <circle cx="50%" cy="50%" r="18" fill="transparent" stroke="#2563eb" strokeWidth="5" strokeDasharray={circumference} strokeDashoffset={offset} strokeLinecap="round" />
        </svg>
        <span className="absolute font-black text-[10px]">{pct}%</span>
      </div>
    );
  };

  return (
    <div className="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-4">
      {ALL_COHORTS.slice(0, 12).map((cohort, i) => {
        const yieldVal = Math.floor(Math.random() * 25) + 70;
        return (
          <div key={i} className="bg-white p-6 rounded-[2rem] shadow-sm border border-slate-100 flex items-center justify-between">
            <div>
              <h5 className="font-black text-slate-900 text-sm">{cohort}</h5>
              <p className="text-slate-400 text-[9px] font-bold uppercase">Yield</p>
            </div>
            {renderPie(yieldVal)}
          </div>
        );
      })}
      <div className="bg-slate-50 p-6 rounded-[2rem] border border-dashed border-slate-200 flex items-center justify-center">
        <span className="text-slate-400 font-bold text-xs">+{ALL_COHORTS.length - 12} more cohorts</span>
      </div>
    </div>
  );
};

const CourseUI = ({ courses }) => (
  <div className="bg-white rounded-[3rem] p-10 shadow-sm border border-slate-100">
    <div className="flex justify-between items-center mb-10">
      <h3 className="text-2xl font-black text-slate-900">Curriculum Matrix</h3>
      <button className="bg-blue-600 text-white px-6 py-3 rounded-2xl text-xs font-black">+ Add Module</button>
    </div>
    <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
      {courses.map(c => (
        <div key={c.id} className="p-6 border border-slate-100 rounded-3xl hover:bg-slate-50 transition-all flex justify-between items-start">
          <div>
            <div className="text-blue-600 font-black text-xs mb-1 uppercase tracking-widest">{c.code}</div>
            <div className="text-lg font-black text-slate-900 mb-2">{c.name}</div>
          </div>
          <div className="flex gap-2">
            <button className="p-2 text-slate-400 hover:text-blue-600 bg-white border border-slate-100 rounded-lg"><Edit3 className="w-4 h-4" /></button>
            <button className="p-2 text-slate-400 hover:text-red-600 bg-white border border-slate-100 rounded-lg"><Trash2 className="w-4 h-4" /></button>
          </div>
        </div>
      ))}
    </div>
  </div>
);

const RegistryUI = ({ students, onDelete, onEdit, downloadCSVTemplate }) => (
  <div className="bg-white rounded-[3rem] shadow-sm border border-slate-100 overflow-hidden">
    <div className="p-10 border-b border-slate-50 flex justify-between items-center bg-slate-50/30">
      <div>
        <h3 className="font-black text-2xl text-slate-900">Student Directory</h3>
        <p className="text-xs text-slate-400 mt-1 font-bold uppercase tracking-wider">Cohort Grouping & Enrollment</p>
      </div>
      <div className="flex gap-3">
        <button 
          onClick={downloadCSVTemplate}
          className="bg-white text-slate-900 border border-slate-200 px-6 py-4 rounded-2xl text-xs font-black flex items-center gap-2 hover:bg-slate-50"
        >
          <Download className="w-4 h-4" /> TEMPLATE
        </button>
        <button className="bg-blue-600 text-white px-8 py-4 rounded-2xl text-xs font-black flex items-center gap-2 shadow-lg shadow-blue-200">
          <Upload className="w-4 h-4" /> BULK UPLOAD
        </button>
      </div>
    </div>
    <div className="overflow-x-auto">
      <table className="w-full text-left">
        <thead className="bg-slate-50 text-[10px] font-black text-slate-400 uppercase tracking-widest">
          <tr>
            <th className="px-10 py-6">Student Identity</th>
            <th className="px-10 py-6">Active Cohort</th>
            <th className="px-10 py-6">Engagement Score</th>
            <th className="px-10 py-6 text-right">Actions</th>
          </tr>
        </thead>
        <tbody className="divide-y divide-slate-50">
          {students.map(s => (
            <tr key={s.id} className="hover:bg-slate-50/50 transition-colors">
              <td className="px-10 py-8">
                <div className="font-black text-slate-900">{s.fname} {s.lname}</div>
                <div className="text-[10px] text-slate-400 font-mono">{s.matric}</div>
              </td>
              <td className="px-10 py-8 text-xs font-black text-blue-600">{s.cohort}</td>
              <td className="px-10 py-8">
                <div className="flex items-center gap-3">
                  <div className="w-16 h-1 bg-slate-100 rounded-full">
                    <div className="h-full bg-blue-600" style={{ width: `${s.yield}%` }}></div>
                  </div>
                  <span className="text-xs font-black">{s.yield}%</span>
                </div>
              </td>
              <td className="px-10 py-8 text-right space-x-1">
                <button className="p-3 text-slate-400 hover:text-blue-600 transition-colors"><Edit3 className="w-4 h-4" /></button>
                <button onClick={() => onDelete(s.id)} className="p-3 text-slate-400 hover:text-red-600 transition-colors"><Trash2 className="w-4 h-4" /></button>
              </td>
            </tr>
          ))}
        </tbody>
      </table>
    </div>
  </div>
);

const ActivateUI = ({ ALL_COHORTS, SEMESTERS, YEARS, MONTHS, courses, showToast, attendanceMode, setAttendanceMode, filters, handleFilterChange }) => (
  <div className="grid grid-cols-1 lg:grid-cols-2 gap-10 max-w-7xl mx-auto">
    <div className="bg-white p-10 rounded-[3rem] shadow-sm border border-slate-100 flex flex-col">
      <h3 className="text-2xl font-black text-slate-900 mb-8">Session Initiation</h3>
      
      <div className="space-y-6 flex-1">
        <div className="grid grid-cols-2 gap-4 p-6 bg-slate-50 rounded-[2.5rem] border border-slate-100">
          <div className="col-span-2 text-[10px] font-black text-slate-400 uppercase tracking-widest mb-2 flex items-center gap-2">
            <Calendar className="w-3 h-3" /> Time-Space Parameters
          </div>
          <div>
            <label className="text-[9px] font-bold text-slate-400 uppercase">Target Cohort</label>
            <select value={filters.cohort} onChange={(e) => handleFilterChange('cohort', e.target.value)} className="w-full bg-white p-3 rounded-xl font-bold text-xs mt-1 border-none outline-none">
              {ALL_COHORTS.map(c => <option key={c}>{c}</option>)}
            </select>
          </div>
          <div>
            <label className="text-[9px] font-bold text-slate-400 uppercase">Academic Module</label>
            <select value={filters.course} onChange={(e) => handleFilterChange('course', e.target.value)} className="w-full bg-white p-3 rounded-xl font-bold text-xs mt-1 border-none outline-none">
              {courses.map(c => <option key={c.code} value={c.code}>{c.code} - {c.name}</option>)}
            </select>
          </div>
          <div className="col-span-2 grid grid-cols-3 gap-3 pt-2 border-t border-slate-100">
            <div>
              <label className="text-[9px] font-bold text-slate-400 uppercase">Year</label>
              <select value={filters.year} onChange={(e) => handleFilterChange('year', e.target.value)} className="w-full bg-white p-2 rounded-lg font-bold text-xs mt-1 outline-none">
                {YEARS.map(y => <option key={y}>{y}</option>)}
              </select>
            </div>
            <div>
              <label className="text-[9px] font-bold text-slate-400 uppercase">Month</label>
              <select value={filters.month} onChange={(e) => handleFilterChange('month', e.target.value)} className="w-full bg-white p-2 rounded-lg font-bold text-xs mt-1 outline-none">
                {MONTHS.map(m => <option key={m}>{m}</option>)}
              </select>
            </div>
            <div>
              <label className="text-[9px] font-bold text-slate-400 uppercase">Semester</label>
              <select value={filters.semester} onChange={(e) => handleFilterChange('semester', e.target.value)} className="w-full bg-white p-2 rounded-lg font-bold text-xs mt-1 outline-none">
                {SEMESTERS.map(s => <option key={s}>{s}</option>)}
              </select>
            </div>
          </div>
        </div>

        <div>
          <label className="text-[10px] font-black text-slate-400 uppercase tracking-widest">Attendance Mode Preference</label>
          <div className="grid grid-cols-2 gap-3 mt-2">
            <button 
              onClick={() => setAttendanceMode('physical')}
              className={`flex items-center justify-center gap-3 p-4 rounded-2xl font-bold transition-all border ${attendanceMode === 'physical' ? 'bg-blue-600 text-white border-blue-600 shadow-lg' : 'bg-slate-50 text-slate-400 border-slate-100'}`}
            >
              <UserCheck className="w-4 h-4" /> Physical Class
            </button>
            <button 
              onClick={() => setAttendanceMode('virtual')}
              className={`flex items-center justify-center gap-3 p-4 rounded-2xl font-bold transition-all border ${attendanceMode === 'virtual' ? 'bg-indigo-600 text-white border-indigo-600 shadow-lg' : 'bg-slate-50 text-slate-400 border-slate-100'}`}
            >
              <Globe className="w-4 h-4" /> Virtual Hub
            </button>
          </div>
        </div>
      </div>

      <button 
        onClick={() => showToast(`Broadcasting Dynamic QR for ${filters.cohort} | ${filters.course}`)} 
        className="w-full bg-slate-900 text-white p-6 rounded-[2rem] font-black shadow-xl hover:bg-slate-800 transition-all uppercase mt-8 flex items-center justify-center gap-3"
      >
        <QrCode className="w-5 h-5" /> Generate Attendance Token
      </button>
    </div>

    {/* Student View Mockup */}
    <div className="flex flex-col">
      <div className="flex items-center gap-2 mb-4 px-4">
        <Smartphone className="w-4 h-4 text-slate-400" />
        <span className="text-[10px] font-black text-slate-400 uppercase tracking-widest">Live Student Interface</span>
      </div>
      <div className="bg-slate-900 rounded-[3.5rem] p-4 shadow-2xl relative aspect-[9/18] max-w-[320px] mx-auto border-[6px] border-slate-800">
        <div className="absolute top-0 left-1/2 -translate-x-1/2 w-24 h-6 bg-slate-800 rounded-b-2xl z-10"></div>
        <div className="bg-white h-full rounded-[2.5rem] overflow-hidden flex flex-col">
           <div className={`p-8 text-white transition-all duration-500 ${attendanceMode === 'virtual' ? 'bg-indigo-600' : 'bg-blue-600'}`}>
              <div className="w-10 h-10 bg-white/20 rounded-lg flex items-center justify-center mb-4"><ShieldCheck className="w-6 h-6" /></div>
              <h4 className="font-black text-xl uppercase tracking-tighter">Register Presence</h4>
              <p className="text-[9px] text-white/70 font-bold uppercase tracking-wide">{filters.course} • {filters.cohort}</p>
           </div>
           
           <div className="p-6 flex-1 flex flex-col gap-5">
              <div className="space-y-1">
                 <label className="text-[9px] font-black text-slate-400 uppercase tracking-widest">Participation Format</label>
                 <div className="flex gap-2">
                    <button 
                      onClick={() => setAttendanceMode('physical')}
                      className={`flex-1 p-3 rounded-xl border text-[10px] font-black transition-all ${attendanceMode === 'physical' ? 'bg-blue-600 border-blue-600 text-white shadow-md' : 'bg-white border-slate-100 text-slate-400'}`}
                    >
                      PHYSICAL
                    </button>
                    <button 
                      onClick={() => setAttendanceMode('virtual')}
                      className={`flex-1 p-3 rounded-xl border text-[10px] font-black transition-all ${attendanceMode === 'virtual' ? 'bg-indigo-600 border-indigo-600 text-white shadow-md' : 'bg-white border-slate-100 text-slate-400'}`}
                    >
                      VIRTUAL
                    </button>
                 </div>
              </div>

              <div className="p-4 bg-slate-50 border border-slate-100 rounded-2xl">
                <div className="text-[9px] font-black text-slate-400 uppercase mb-2">Session Details</div>
                <div className="text-xs font-black text-slate-900">{filters.semester} {filters.year}</div>
                <div className="text-[10px] font-bold text-slate-500 mt-0.5">{filters.month} Class Matrix</div>
              </div>

              <button className={`mt-auto w-full text-white p-5 rounded-2xl text-[10px] font-black uppercase tracking-widest shadow-xl transition-all ${attendanceMode === 'virtual' ? 'bg-indigo-600' : 'bg-slate-900'}`}>Confirm Entry</button>
           </div>
           <div className="h-1.5 w-1/3 bg-slate-100 mx-auto mb-4 rounded-full"></div>
        </div>
      </div>
    </div>
  </div>
);

const MatrixUI = ({ students, filters }) => {
  const sessions = Array.from({ length: 10 }, (_, i) => `L${i + 1}`);
  return (
    <div className="bg-white rounded-[3rem] shadow-sm border border-slate-100 overflow-hidden">
      <div className="p-10 border-b border-slate-50 bg-slate-50/30 flex justify-between items-center">
        <div>
          <h3 className="font-black text-2xl text-slate-900">Session Engagement Matrix</h3>
          <div className="flex gap-2 mt-2">
            <span className="px-2 py-1 bg-blue-100 text-blue-700 text-[10px] font-black rounded uppercase">{filters.cohort}</span>
            <span className="px-2 py-1 bg-slate-200 text-slate-700 text-[10px] font-black rounded uppercase">{filters.course}</span>
          </div>
        </div>
        <button className="bg-white border border-slate-200 p-4 rounded-2xl text-slate-400 hover:text-blue-600 transition-colors">
          <Download className="w-5 h-5" />
        </button>
      </div>
      <div className="overflow-x-auto">
        <table className="w-full text-left min-w-[800px]">
          <thead>
            <tr className="bg-slate-50 text-[9px] font-black text-slate-400 uppercase tracking-widest">
              <th className="px-10 py-6 sticky left-0 bg-slate-50 z-10 border-r border-slate-100">Participant</th>
              {sessions.map(s => <th key={s} className="px-2 py-6 text-center">{s}</th>)}
            </tr>
          </thead>
          <tbody className="divide-y divide-slate-50">
            {students.filter(s => s.cohort === filters.cohort || true).map(s => (
              <tr key={s.id} className="hover:bg-slate-50/50">
                <td className="px-10 py-6 sticky left-0 bg-white z-10 border-r border-slate-100">
                  <div className="font-bold text-slate-900 text-xs">{s.fname} {s.lname}</div>
                  <div className="text-[9px] text-slate-400 font-mono">{s.matric}</div>
                </td>
                {sessions.map((_, i) => (
                  <td key={i} className="px-2 py-6">
                    <div className={`w-7 h-7 mx-auto rounded-lg transition-all ${Math.random() > 0.3 ? 'bg-blue-600 shadow-lg shadow-blue-100' : 'bg-slate-100'}`}></div>
                  </td>
                ))}
              </tr>
            ))}
          </tbody>
        </table>
      </div>
    </div>
  );
};

export default App;
